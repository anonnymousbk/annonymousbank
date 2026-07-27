<p align="center">
  <img src="https://img.shields.io/badge/Status-Ativo%20%26%20Seguro-brightgreen?style=for-the-badge&logo=shield" alt="Status">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Plataforma-Termux%20%2F%20Android-orange?style=for-the-badge&logo=android" alt="Plataforma">
  <img src="https://img.shields.io/badge/Vers%C3%A3o-v6.5%20Commerce-cyan?style=for-the-badge" alt="Versao">
</p>

<h1 align="center">⚡ ANONYMOUS BANK PIX TERMINAL v6.5</h1>
<h3 align="center">Plataforma Financeira PIX Integrada para Termux & Android</h3>

<p align="center">
  Sistema financeiro completo, responsivo e de alta performance projetado para dispositivos móveis via Termux. Permite cobranças instantâneas por QR Code PIX, saques com aprovação automática, gestão de saldo individual e monitoramento em tempo real com suporte a notificações push nativas no Android.
</p>

---

## ✨ Principais Funcionalidades

### 📥 1. Cobrança PIX Instantânea (Cash-In)
- **QR Code Unicode de Alta Definição**: Renderização ultracompacta em meio-bloco (`▀`, `▄`, `█`) perfeitamente ajustada para telas de smartphones.
- **Copia e Cola Automático**: Copia a chave do PIX diretamente para a área de transferência do celular (`termux-clipboard-set`).
- **Monitor de Recebimento em Tempo Real**: Checagem contínua via polling com alerta imediato de pagamento efetuado.
- **Crédito em Saldo Individual**: Desconto automático da taxa fixa de gateway de **R$ 0,50** por depósito com crédito líquido imediato na conta.

### 📤 2. Solicitação de Saque & Resgate (Cash-Out)
- **Suporte a Todas as Chaves PIX**: Validação estrita para CPF, CNPJ, E-mail, Telefone e Chave Aleatória (EVP / UUID).
- **Robô de Saque Automático (Auto-Payout Engine)**: Saques a partir do limite configurado são aprovados e pagos instantaneamente via PIX sem espera.
- **Trava de Segurança Anti-Saque Duplo**: Reserva atômica de saldo no servidor durante a solicitação para evitar saques duplos ou saldo negativo.
- **Fila de Aprovação**: Solicitações abaixo do limite ficam pendentes de aprovação na fila administrativa com opção de reembolso garantido caso recusadas.

### 💰 3. Gestão de Saldo & Perfil Individual
- **Painel Executivo da Conta**: Exibe saldo disponível, total depositado bruto, total sacado e prazo de validade da licença comercial em tempo real.
- **Tabela de Taxas Transparente**: Visualização clara das tarifas do gateway.

### 📊 4. Extrato & Histórico de Transações
- **Banco de Dados Local SQLite**: Armazenamento seguro de todas as movimentações financeiras localmente (`transactions.db`).
- **Filtros e Pesquisas Avançadas**: Pesquisa instantânea por ID, Nome do Pagador, CPF/CNPJ ou Tipo de Transação.

### 🔔 5. Notificações Push & Vibração Nativas
- **Alertas no Celular**: Disparo de notificações na barra do Android via `termux-notification`.
- **Feedback Háptico**: Vibração do celular (`termux-vibrate`) ao receber depósitos ou saques.
- **Central de Notificações Cloud**: Recebimento de avisos diretos e comunicados gerais enviados pelo administrador.

### 🤖 6. Robô Sentinel de Segurança de Sessão
- **Monitoramento Daemon Thread**: Robô em segundo plano que verifica a validade da licença e o status da conta a cada 8 segundos.
- **Desconexão Automática**: Se a licença expirar ou o acesso for bloqueado pelo administrador, o robô encerra a sessão na hora, protegendo a plataforma.

### 🚀 7. Atualizações Automáticas (OTA)
- **Instalação em 1 Clique**: O aplicativo verifica atualizações no servidor ao logar. Se houver nova versão, baixa e instala o pacote ZIP automaticamente.
- **Checagem Inteligente Semver**: O aviso de atualização só é exibido se a versão do servidor for estritamente mais recente que a já instalada.

---

## 📲 Instalação Otimizada no Termux (1 Comando)

### Passo 1: Preparar o Ambiente Termux
Abra o seu aplicativo **Termux** no Android e execute os comandos abaixo para instalar o Python e as dependências necessárias:

```bash
pkg update -y && pkg install -y python python-pip curl termux-api
pip install qrcode colorama
```

### Passo 2: Baixar e Instalar o Sistema
Extraia o pacote do aplicativo na pasta do Termux e execute o instalador oficial:

```bash
cd AnnonymousBank
chmod +x install.sh
./install.sh
```

---

## ⚡ Atalhos Globais de Acesso

Após a execução do `./install.sh`, o sistema registra executáveis globais no seu Termux. Você pode abrir o aplicativo em **QUALQUER aba ou pasta** digitando simplesmente:

```bash
anon
```
ou
```bash
bank
```
ou
```bash
anonbank
```

---

## 🚀 Como Usar o Aplicativo

### 🔐 1. Tela de Login e Suporte
Ao abrir o sistema (`anon`), você verá a tela de acesso:
- Digite **`1`** para fazer login com o seu **Usuário** e **Senha**.
- Digite **`2`** para entrar em contato com o **Suporte Comercial no WhatsApp** (abre o WhatsApp automaticamente no seu celular).

```text
┌──────────────── PORTAL DE ACESSO ANONYMOUS BANK ────────────────┐
│ 🔐 SISTEMA DE AUTENTICAÇÃO COMERCIAL SAAS                       │
│                                                                 │
│   [1] 🔐 Entrar no Sistema                                      │
│   [2] 💬 Falar com Suporte Comercial (WhatsApp)                 │
│   [0] 🚪 Sair                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### 📥 2. Gerando uma Cobrança PIX
1. No menu principal, digite a opção **`1`** (`Cobrar via PIX`).
2. Digite o valor em R$ (Ex: `15.00`).
3. O sistema gerará o **QR Code na tela** e copiará o código **PIX Copia e Cola** para a sua área de transferência.
4. O monitor de recebimento começará a checar automaticamente. Assim que o pagamento for feito, o saldo será creditado na sua conta com alerta de som e vibração!

### 📤 3. Solicitando um Saque
1. No menu principal, escolha a opção **`2`** (`Solicitar Saque / Resgate`).
2. Escolha o tipo da sua chave PIX (CPF, CNPJ, E-mail, Telefone ou Chave Aleatória).
3. Digite a sua chave PIX e confirme a operação.
4. Se o **Robô de Saque Automático** estiver ativo, o valor será enviado para a sua conta bancária no mesmo segundo!

---

## 📂 Estrutura de Arquivos da Versão Usuário

```text
AnnonymousBank/
├── main.pyc               # Executável Principal e Interface da Conta
├── config.json            # Configurações do Aplicativo e Versão
├── install.sh             # Script de Instalação e Criação de Atalhos no Termux
├── core/
│   ├── auth.pyc           # Autenticação, Ledger de Saldo e Robô Sentinel
│   ├── banner.pyc         # Banners ASCII Executivos Responsivos
│   ├── db.pyc             # Banco de Dados Local SQLite (transactions.db)
│   ├── notifier.pyc       # Notificações Push e Vibração Nativas no Android
│   ├── qrcode_gen.pyc     # Gerador de QR Code Unicode Meio-Bloco
│   ├── ui.pyc             # Sistema de Cores ANSI, Caixas Responsivas e Spinners
│   └── updater.pyc        # Atualizador Automático de Pacotes ZIP (OTA)
└── modules/
    ├── misticpay.pyc      # Conector e Cliente da Rede de Pagamentos PIX
    └── transaction_history.pyc # Extrato e Histórico de Transações
```

---

## 🔒 Segurança e Privacidade White-Label

- **Bytecode Binário Protegido**: Todos os arquivos de código-fonte Python foram compilados em Bytecode `.pyc` para evitar cópias não autorizadas ou adulteração de arquivos.
- **Interface White-Label**: Interface limpa e totalmente profissional sem exibição de termos técnicos de infraestrutura ou servidores internos.
- **Criptografia Cloud Vault**: As credenciais mestres da API são mantidas em um cofre na nuvem, garantindo total segurança durante as transações.

---

<p align="center">
  <b>Annonymous Bank Financial Systems &copy; 2026 - Todos os Direitos Reservados</b>
</p>
