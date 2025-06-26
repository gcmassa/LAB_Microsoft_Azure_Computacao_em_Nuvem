# LAB_Microsoft_Azure_Computacao_em_Nuvem - DESAFIO
# 🗄️ Passo a Passo: Configurar uma Instância de Banco de Dados no Azure (Azure SQL)

## 1. Acessar o Portal do Azure
- Vá para: [https://portal.azure.com](https://portal.azure.com)
- Faça login com sua conta Microsoft

## 2. Criar um Grupo de Recursos (opcional)
- Menu lateral > **"Grupos de recursos"** > **"Criar"**
- Informe:
  - Nome (ex: `rg-database`)
  - Região (ex: Brasil Sul)
- Clique em **"Revisar + Criar"** > **"Criar"**

## 3. Criar um Servidor SQL
- Vá para **"SQL Servers"** > **"Criar"**
- Preencha os campos:
  - Nome do servidor (ex: `sql-servidor`)
  - Login e senha do administrador
  - Região (mesma do grupo de recursos)
- Clique em **"Revisar + Criar"** > **"Criar"**

## 4. Criar o Banco de Dados SQL

### 🔹 Aba: Básico
- Menu > **"SQL Databases"** > **"Criar"**
- Preencha:
  - Assinatura e Grupo de Recursos
  - Nome do banco (ex: `db-empresa`)
  - Selecione o **Servidor SQL** criado anteriormente
  - **Camada de serviço:** Basic, Standard, Premium ou vCores
  - Defina tamanho e desempenho (DTUs/vCores)

### 🔹 Aba: Rede
- Escolha a conectividade:
  - **Acesso público** (por IP externo)
  - **Acesso privado** (via VNet – mais seguro)
- Regras de firewall:
  - Adicione seu IP para acesso externo

### 🔹 Aba: Segurança
- **Autenticação:**
  - SQL (usuário e senha) ou Entra ID (opcional)
- **Criptografia:**
  - Ativar **TDE (Transparent Data Encryption)**
- **Auditoria:** configurar se necessário

### 🔹 Aba: Backup
- Retenção de backup (7 a 35 dias)
- **Geo-replicação** (opcional, para alta disponibilidade)

### 🔹 Aba: Tags (opcional)
- Adicione **tags** para organização e controle de custo

### 🔹 Aba: Revisar + Criar
- Revise todas as configurações
- Clique em **"Criar"**

## 5. Aguardar a Implantação
- Acompanhe o provisionamento do banco no painel

## 6. Conectar-se ao Banco de Dados
- Acesse a instância criada > **"Mostrar cadeia de conexão"**
- Utilize:
  - **Azure Data Studio**
  - **SQL Server Management Studio (SSMS)**
  - **DBeaver**, entre outros
- Insira:
  - Servidor, banco, usuário e senha definidos

## 7. Boas Práticas de Segurança
- Restringir IPs no firewall
- Habilitar autenticação multifator (MFA)
- Monitorar acessos com **Microsoft Defender for SQL**
- Configurar **roles e permissões específicas**
