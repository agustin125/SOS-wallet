# 🌐 SOS wallet – Decentralized Wallet with SMS + Blockchain Transfers

SOS Wallet is a powerful open-source decentralized wallet designed to maximize accessibility, scalability, and cross-chain interoperability. It combines a robust software architecture with an SMS-based transfer layer, enabling users to perform blockchain transactions even in low-connectivity environments.

Its most recent and significant feature is the integration of the Fisher Capture mechanism, focused on the validation and secure submission of advanced transactions to the EVVM network.

## 🔋 Key Features

### 🔐 Security & Access
* **Dual Access (SMS & HTTP):** Interact with your wallet via **HTTP endpoints** (Web/API) or through **SMS messages** (using providers like Vonage or Twilio).
* **Modular Architecture:** Open-source design with clear **Separation of Concerns** (SoC) and a strong focus on cryptographic security.
* **Swagger Integration:** Local interface for comprehensive documentation and easy testing of all **API endpoints**.

### 🔗 Blockchain Interoperability
* **Multi-Network Support (Cross-Chain):** Engineered for secure token transfers across multiple Blockchain networks.

### 🎣 EVVM Fisher Capture (New!)
* **Advanced Capture:** A dedicated interface (`fisher-capture.tsx`) for creating, validating, and signing transactions using the **EIP-191 standard**.
* **Direct EVVM Submission:** Transmission of validated and signed transactions directly to the **EVVM Network**.
* **PayVVM Integration:** UI follows the PayVVM design pattern for clear user flow and effective state management.

  ## 🏗️ Technical Architecture and Data Flow

SOS Wallet is structured into modules to handle the complexity of the dual environment (SMS/Web) and cross-chain interactions.

### Core Components

**Transaction Abstraction** | Core logic for handling *cross-chain* token transfers and *gas* estimation. | `transactions/` |
| **Network Providers** | Handles specific network connections, *signing*, and RPC calls (e.g., Ethereum, Polygon). | `network-providers/` |
| **SMS Service** | Logic for routing, *parsing*, and sending messages via SMS providers (e.g., Vonage, Twilio). | `sms-service/` |
| **Fisher Utilities** | **NEW:** Cryptographic utilities for **EIP-191 message** generation, validation, and analysis. | `fisher-utils.ts` |
| **Fisher Capture UI** | **NEW:** Frontend component for the transaction capture, signing, and submission workflow. | `fisher-capture.tsx` |

### Fisher Capture Workflow Highlight

The **Fisher Capture** interface is prominently featured on the *homepage*, preceding the MATE control panel, underscoring its role in advanced transaction validation:

1.  User defines transaction details in the `fisher-capture.tsx` UI.
2.  `fisher-utils.ts` generates the **EIP-191 signature message**.
3.  Transaction is signed (simulating a Web3 wallet integration).
4.  The system performs a **validation check** for format and integrity.
5.  The signed and validated transaction is securely submitted to the **EVVM Network**.

---

## 🚀 Getting Started

### 1. Prerequisites
* Node.js (v16+)
* npm (v8+)

### 2. Installation

Clone the repository and install dependencies:

```bash
git clone [https://github.com/tu-usuario/sos-wallet.git](https://github.com/tu-usuario/sos-wallet.git)
cd sos-wallet
npm install
3. Environment Configuration
Create your secure environment file from the example. Do NOT commit .env to Git.

Bash

cp .env.example .env
Edit the .env file to include your sensitive credentials (API keys, RPC URLs, etc.).

4. Running the Project
Start the application in development mode:

Bash

npm run start
The API and web UI will be available, and you can access Swagger UI for endpoint testing.

5. Running Tests
Execute the full testing suite, including the core transaction logic and Fisher utilities:

Bash

npm run test

##🤝 Contributions

SOS Wallet is a community-driven, open-source project. We welcome and encourage all contributions, including bug fixes, feature enhancements, and documentation improvements.
Fork the repository.

Create a new feature branch (git checkout -b feature/AmazingFeature).

Commit your changes (git commit -m 'Add some AmazingFeature').

Push to the branch (git push origin feature/AmazingFeature).

Open a Pull Request.

Please review our CONTRIBUTING.md (if you plan to add one) for detailed guidelines.

## 🪲 Run tests

`npm run test`
