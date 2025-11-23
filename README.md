# 🌐 SOS wallet – Decentralized Wallet with SMS + Blockchain Transfers

SOS Wallet is a powerful open-source decentralized wallet designed to maximize accessibility, scalability, and cross-chain interoperability. It combines a robust software architecture with an SMS-based transfer layer, enabling users to perform blockchain transactions even in low-connectivity environments.

Its most recent and significant feature is the integration of the Fisher Capture mechanism, focused on the validation and secure submission of advanced transactions to the EVVM network.

## 🔋 Key Features

**Dual Access (SMS & HTTP):** Interact with your wallet via HTTP endpoints (for Web/API) or through SMS messages (using providers like Vonage or Twilio), making token transfer truly ubiquitous.

**Multi-Network Support (Cross-Chain):** Engineered for secure token transfers across multiple Blockchain networks.

**Fisher Capture Mechanism (EVVM):**

**Advanced Capture:** A dedicated interface for creating, validating, and signing transactions using the EIP-191 standard.

**Direct EVVM Submission:** Direct transmission of validated transactions to the EVVM Network.

**PayVVM Integration:** UI follows the PayVVM design pattern for clear user flow and effective state management.

**Modular and Secure Architecture:** Open-source design with clear Separation of Concerns (SoC) and a strong focus on cryptographic security.

**Swagger Integration:** Local interface for comprehensive documentation and easy testing of all API endpoints.

**Future-Ready:** Technology base prepared to integrate AI-driven validations (Transaction Intelligence).

## 🚀 How It Works

- Users can interact with the wallet via HTTP endpoints or by sending SMS messages.
- All blockchain interactions are handled by network-specific providers.
- The `transactions/` module abstracts cross-chain token transfers.
- Incoming SMS messages are parsed and routed to appropriate services.


## 📦  Install project

`npm install`

## 📄 Configure Environment Variables

Create a .env file in the root directory of your project. You can use the provided .env.example file as a template.

`cp .env.example .env`

## 🏃 Run project 

`npm run start`

## 🪲 Run tests

`npm run test`
