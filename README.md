```markdown
# 📱 LIA App – Assistente Telefônica com IA

**LIA (Ligação Inteligente Autônoma)** é um aplicativo de atendimento automático com inteligência artificial, integrado ao backend `lia-rest`, que recebe chamadas via Twilio, conversa com o chamador e transborda para o usuário se necessário.

Este repositório contém o **app mobile React Native (CLI com TypeScript)**, compatível com Twilio Voice SDK, Firebase Push Notification e APIs nativas.

---

## ⚙️ Tecnologias Utilizadas

| Componente         | Tecnologia                            |
|--------------------|----------------------------------------|
| App mobile         | React Native (Expo ejected) + TypeScript |
| Navegação          | React Navigation                      |
| VoIP               | Twilio Voice SDK (iOS/Android)        |
| Notificações Push  | Firebase Cloud Messaging (FCM)        |
| Gerenciamento de estado | Redux Toolkit ou Context API       |
| Backend            | Integração com [`lia-rest`](https://github.com/Neocoode/lia-rest)

---

## 📁 Estrutura do Projeto

```

lia-app/
├── App.tsx
├── ios/                     # Projeto iOS nativo (pós-eject)
├── android/                 # Projeto Android nativo
├── screens/                 # Telas principais
│   ├── Home.tsx
│   ├── IncomingCall.tsx
│   └── Recado.tsx
├── services/
│   ├── twilio.ts            # Configuração do Twilio Voice SDK
│   ├── firebase.ts          # Setup de FCM
│   └── api.ts               # Comunicação com backend REST
├── store/                   # Redux store (opcional)
├── assets/
│   └── logo/lia-logo.svg
├── app.json / eas.json      # Configuração do Expo
└── README.md

````

---

## 🚀 Como Rodar o App

### Pré-requisitos

- Node.js 18+
- Expo CLI (`npm install -g expo-cli`)
- CocoaPods (`brew install cocoapods`)
- Dispositivo físico conectado (recomendado)
- Firebase configurado
- Conta Twilio com número ativo

---

### Instalação

```bash
git clone https://github.com/seu-usuario/lia-app.git
cd lia-app
yarn install
````

### Após o Eject

```bash
npx expo prebuild
cd ios
pod install
cd ..
```

---

### Rodar no Device

#### Android:

```bash
npx react-native run-android
```

#### iOS:

```bash
npx react-native run-ios --device
```

---

## 🔐 Integrações

### 🔸 Firebase Push Notification

* Notifica o app se a chamada for considerada prioritária
* Integração com `firebase-admin` no backend

### 🔸 Twilio Voice SDK

* Permite atender chamadas no app
* Suporte a conferência e chamadas VoIP

---

## 🔗 Integração com Backend

Este app se comunica com a API `lia-rest`, responsável por:

* Receber webhooks do Twilio
* Decidir se a chamada será transbordada
* Criar conferência e enviar push para o app
* Geração de JWT para entrada na call

---

## 📲 Funcionalidades em Desenvolvimento

* [x] Interface básica com React Navigation
* [ ] Integração com Twilio Voice SDK
* [ ] Recebimento de Push (FCM)
* [ ] Tela de chamada com botão "Atender"
* [ ] Visualização de recados/agendamentos

---

## 🧠 Sobre o Projeto

> **LIA** é a mente que atende suas ligações.
> Sua secretária eletrônica com IA integrada a voz e push.

---

## 📝 Licença

Desenvolvido por [Neocoode](https://github.com/neocoode)
Criado com suporte do ChatGPT – Julho 2025

```