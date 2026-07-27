<p align="center">
  <img src="https://img.shields.io/badge/Sistema-PIX%20Commerce-brightgreen?style=for-the-badge&logo=pix" alt="PIX Commerce">
  <img src="https://img.shields.io/badge/KYC-Sem%20KYC-blue?style=for-the-badge" alt="Sem KYC">
  <img src="https://img.shields.io/badge/Plataforma-Termux%20%2F%20Android-orange?style=for-the-badge&logo=android" alt="Plataforma">
  <img src="https://img.shields.io/badge/Vers%C3%A3o-v6.5%20Commerce-cyan?style=for-the-badge" alt="Versao">
</p>

<h1 align="center">⚡ ANONYMOUS BANK PIX TERMINAL v6.5</h1>
<h3 align="center">Aplicativo Comercial de Pagamentos e Recebimentos PIX Sem KYC</h3>

<p align="center">
  Aplicativo financeiro completo, rápido e privado desenvolvido para facilitar suas cobranças por PIX, gestão de saldo individual e solicitações de resgate direto no seu celular Android via Termux. <b>Envie e receba PIX instantaneamente sem burocracia ou verificação de KYC.</b>
</p>

---

## 🎥 Demonstração em Vídeo

 Assista ao vídeo de demonstração do sistema operando em tempo real no Termux:

<p align="center">
  <a href="docs/demo.mp4">
    <img src="docs/images/video_preview.png" alt="Assistir Vídeo de Demonstração" width="700">
  </a>
</p>

> 💡 *Dica: Se o vídeo não abrir diretamente no seu navegador, assista ao arquivo `docs/demo.mp4` ou `docs/demo.gif` incluído no repositório.*

---

## 📸 Galeria de Imagens do Sistema

### 1. Portal de Acesso & Suporte WhatsApp
Interface limpa de autenticação comercial com atalho direto para o atendimento ao cliente via WhatsApp.

<p align="center">
  <img src="docs/images/login_screen.png" alt="Portal de Login e Suporte" width="650">
</p>

```text
┌──────────────── PORTAL DE ACESSO ANONYMOUS BANK ────────────────┐
│ 🔐 SISTEMA DE AUTENTICAÇÃO COMERCIAL SAAS                       │
│                                                                 │
│   [1] 🔐 Entrar no Sistema                                      │
│   [2] 💬 Falar com Suporte Comercial (WhatsApp)                 │
│   [0] 🚪 Sair                                                   │
└─────────────────────────────────────────────────────────────────┘
```

---

### 2. Cobrança PIX Instantânea (Cash-In)
Geração automática de QR Code em alta definição e código Copia e Cola enviado direto para a área de transferência do seu celular.

<p align="center">
  <img src="docs/images/pix_checkout.png" alt="Cobrança PIX e QR Code" width="650">
</p>

```text
┌─────────────────────── COBRANÇA PIX GERADA ───────────────────────┐
│ 💵 Valor a Receber: R$ 25,00                                      │
│ 🔑 Chave Copia/Cola Copiada para a Área de Transferência!        │
│ ⏳ Aguardando pagamento em tempo real...                         │
└───────────────────────────────────────────────────────────────────┘
```

---

### 3. Painel de Saldo & Perfil da Conta
Acompanhe seu saldo em conta disponível, histórico de depósitos, total sacado e validade da sua licença.

<p align="center">
  <img src="docs/images/user_dashboard.png" alt="Painel da Conta e Saldo" width="650">
</p>

```text
┌───────────────────── PAINEL DA CONTA SAAS ─────────────────────┐
│ 👤 Usuário: cliente_vip (CLIENTE) │ API: CONECTADO              │
│ 💰 Seu Saldo Individual: R$ 150,00                             │
└────────────────────────────────────────────────────────────────┘
```

---

## ✨ Recursos do Aplicativo

### 🔒 1. 100% Sem KYC (Zero Burocracia)
- **Envie e Receba PIX Sem KYC**: Sem necessidade de envio de documentos burocráticos, fotos de identidade ou verificações de KYC para movimentar seus fundos.
- **Acesso Imediato**: Cadastre sua licença e comece a operar imediatamente.

### 📥 2. Cobrar via PIX (Gerar QR Code)
- **QR Code na Tela**: Gera QR Codes compactos e em alta definição diretamente no terminal do seu celular.
- **Copia e Cola Automático**: Copia o código PIX Copia e Cola instantaneamente para a área de transferência do seu dispositivo.
- **Monitor de Pagamento em Tempo Real**: Acompanhamento automático da cobrança com alerta visual e sonoro assim que o cliente efetua o pagamento.
- **Crédito em Saldo**: O valor líquido é creditado diretamente no seu saldo disponível em conta.

### 📤 3. Solicitar Saque / Resgate
- **Transferência via PIX**: Resgate seu saldo disponível para qualquer chave PIX (CPF, CNPJ, E-Mail, Telefone ou Chave Aleatória).
- **Processamento Rápido**: Solicitações de resgate com acompanhamento de status em tempo real.

### 💰 4. Meu Saldo e Perfil
- **Painel Financeiro**: Acompanhe seu saldo em conta disponível, histórico de depósitos, total sacado e validade da sua licença de uso.

### 📊 5. Extrato e Histórico
- **Histórico Completo**: Consulte todas as suas movimentações de entrada e saída.
- **Busca por Transação**: Pesquise recibos por valor, tipo ou identificador.

### 🔔 6. Notificações no Celular
- **Alertas no Android**: Notificações nativas no seu celular ao receber pagamentos ou ao ter solicitações de saque concluídas.

### 💬 7. Atendimento e Suporte
- **Atalho Direto para o WhatsApp**: Canal direto de suporte comercial disponível no portal de acesso do aplicativo.

---

## 📲 Como Instalar no Seu Celular (Termux)

### Passo 1: Preparar o Termux
Abra o aplicativo **Termux** no seu celular e digite o comando abaixo para instalar as bibliotecas necessárias:

```bash
pkg update -y && pkg install -y python python-pip curl termux-api
pip install qrcode colorama
```

### Passo 2: Executar a Instalação
Acesse a pasta do aplicativo e rode o comando de instalação:

```bash
cd AnnonymousBank
chmod +x install.sh
./install.sh
```

---

## ⚡ Atalhos de Acesso Rápido

Após a instalação, você pode abrir o aplicativo a qualquer momento abrindo o Termux e digitando:

```bash
anon
```
ou
```bash
bank
```

---

## 🚀 Como Usar o Aplicativo

### 🔐 1. Acessando a Sua Conta
Ao abrir o aplicativo (`anon`), selecione a opção desejada:
- Digite **`1`** para entrar com seu **Usuário** e **Senha**.
- Digite **`2`** para abrir o **Suporte no WhatsApp**.

### 📥 2. Gerando uma Cobrança
1. No menu principal, escolha a opção **`1`** (`Cobrar via PIX`).
2. Digite o valor que deseja cobrar (Exemplo: `20.00`).
3. O QR Code será exibido na tela e a chave Copia e Cola será copiada automaticamente.
4. Assim que o pagamento for concluído pelo cliente, você receberá o aviso de confirmação na tela!

### 📤 3. Solicitando Resgate do Saldo
1. Escolha a opção **`2`** (`Solicitar Saque / Resgate`).
2. Informe o tipo da sua chave PIX e digite sua chave.
3. Digite o valor que deseja sacar do seu saldo disponível.
4. Confirme a operação para enviar a solicitação.

---

<p align="center">
  <b>Anonymous Bank PIX Commerce &copy; 2026 - Todos os Direitos Reservados</b>
</p>
