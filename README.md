# Sify PDV — Tauri

Sistema de PDV da **Sify Sistemas**, feito para rodar em computador Windows e Linux, inclusive em máquina mais simples.

> **pdv-sify-nova-versao-windows-pc-fraco**

## 🚀 Sobre o projeto

Esse projeto é a versão desktop do **Sify PDV**.

A ideia é ter um programa leve para o comércio, sem aquela enrolação toda. O sistema roda o PDV web dentro do aplicativo usando **Tauri**, aproveitando a aplicação que já existe na Sify Sistemas.

O foco é rodar bem até em computador mais fraco, uai. 😄

## 🛠️ Tecnologias

* **Tauri**
* **React**
* **TypeScript**
* **Vite**
* **Rust**
* **PWA**
* **WebView**

O Tauri funciona como a casca do aplicativo. O sistema de vendas continua sendo a aplicação web da Sify.

## 🖥️ Como funciona

A estrutura é basicamente:

```text
Computador
    ↓
Sify PDV — aplicativo Tauri
    ↓
WebView
    ↓
https://pdv.sifysistemas.cloud
```

O aplicativo desktop não precisa reescrever o sistema inteiro. Ele serve como uma interface nativa para executar o PDV.

## 🖨️ Impressão

A impressão é feita através do serviço local da Sify Sistemas.

O PDV conversa com o serviço de impressão pela porta:

```text
http://localhost:8182
```

O serviço local fica responsável pela comunicação com as impressoras.

Assim o Tauri não precisa ficar conversando diretamente com cada modelo de impressora.

## ⌨️ Atalhos

O aplicativo possui atalhos globais para algumas funções do PDV.

Atualmente:

* **F2** → alterna tela cheia

Outros atalhos e funções podem ser adicionados conforme o projeto evoluir.

## 📦 Desenvolvimento

Para instalar as dependências:

```bash
npm install
```

Para iniciar o projeto:

```bash
npx tauri dev
```

Para gerar a versão de produção:

```bash
npx tauri build
```

Os arquivos gerados ficam dentro da pasta de build do Tauri.

## 🎯 Objetivo

O objetivo é transformar o Sify PDV em um aplicativo desktop leve, simples e confiável para pequenos comércios.

A ideia é funcionar sem precisar de um computador da NASA pra abrir o caixa. 😂

**Sify Sistemas — Controle, não burocracia.**

---

Desenvolvido por **Nazareno Soluções**.
