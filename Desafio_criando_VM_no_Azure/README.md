# LAB_Microsoft_Azure_Computacao_em_Nuvem - DESAFIO
# 🚀 Passo a Passo: Criando uma Máquina Virtual no Azure

## 1. Acessar o Portal do Azure
- Acesse: [https://portal.azure.com](https://portal.azure.com)
- Faça login com sua conta Microsoft.

## 2. Criar um Grupo de Recursos (opcional)
- Vá em **"Grupos de recursos"** > **"Criar"**
- Defina um nome e selecione a **região**
- Clique em **"Revisar + Criar"** > **"Criar"**

## 3. Criar a Máquina Virtual
- Vá em **"Máquinas Virtuais"** > **"Criar"** > **"Máquina Virtual do Azure"**

### 🔹 Aba: Básico

#### 🔸 Detalhes do Projeto
- **Assinatura:** selecione a sua
- **Grupo de Recursos:** selecione um existente ou crie um novo

#### 🔸 Detalhes da Instância
- **Nome da VM:** ex: `vm-giancarlo`
- **Região:** ex: Brasil Sul

#### 🔸 Opções de Disponibilidade
- **Nenhuma infraestrutura de redundância**
- **Conjunto de disponibilidade**
- **Zona de disponibilidade**

#### 🔸 Opções de Zona
- **Selecionar zona manualmente:** (Zona 1, 2 ou 3)
- **Deixar o Azure escolher automaticamente**

> **Obs:** nem todas as regiões têm suporte para zonas de disponibilidade.

#### 🔸 Sistema e Autenticação
- **Imagem:** ex: Windows Server ou Ubuntu
- **Tamanho:** ex: B1s para testes
- **Usuário/senha** ou **chave SSH**
- **Portas de entrada:** habilite RDP (Windows) ou SSH (Linux)

### 🔹 Aba: Disco
- Tipo de disco: **SSD padrão** recomendado

### 🔹 Aba: Rede
- Configurar rede virtual, IP público e regras de segurança
- Habilitar acesso remoto conforme o sistema

### 🔹 Aba: Gerenciamento
- Configurar desligamento automático, monitoramento, backup (opcional)

### 🔹 Aba: Revisar + Criar
- Verifique as configurações
- Clique em **"Criar"**

## 4. Implantação
- Acompanhe o progresso da criação da VM (leva alguns minutos)

## 5. Conexão à VM
- Acesse a VM através de:
  - **RDP** (Windows)
  - **SSH** (Linux)
- Use o **IP público** e as **credenciais** definidas