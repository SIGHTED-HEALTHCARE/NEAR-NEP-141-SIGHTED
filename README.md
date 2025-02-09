# **SIGHTED Token on NEAR blockchain (NEP-141)**  
A **NEP-141-compliant token** on the **NEAR blockchain** designed for privacy-centric applications and token-based access control.

---

## **Overview**  
**SIGHTED Token** is a **fungible token** built on the **NEAR blockchain**, following the **NEP-141 standard**. This token is intended for use in privacy-preserving decentralized applications (dApps) to enable secure data access, reward mechanisms, and cross-chain interoperability.

---

## **Features**
- **NEP-141 Standard**: Fully compliant with NEAR's NEP-141 fungible token standard.
- **Minting & Burning**: Support for minting and burning tokens.
- **Cross-Chain Compatibility**: Future integration with external chains for interoperability.
- **Privacy-Focused**: Designed for integration with privacy solutions like **Calimero private shards** and ZKP-based dApps.
- **Scalable & Low-Cost**: Built on the NEAR blockchain for fast, low-cost transactions.

---

## **Installation**
### Prerequisites
- Node.js (>= 14.x)
- NEAR CLI installed  
  ```bash
  npm install -g near-cli
  ```

### Clone the Repository
```bash
git clone https://github.com/your-repo/NEAR-NEP-141-SIGHTED.git
cd NEAR-NEP-141-SIGHTED
```

### Install Dependencies
```bash
npm install
```

---

## **Usage**
### Deploying the Contract
1. **Build the contract**:  
   ```bash
   npm run build
   ```

2. **Deploy the contract**:  
   Replace `<your-account.testnet>` with your NEAR testnet account.  
   ```bash
   near deploy --accountId <your-account.testnet> --wasmFile ./build/sighted_token.wasm
   ```

### Interacting with the Token
#### Minting Tokens
```bash
near call <your-account.testnet> mint '{"account_id": "receiver.testnet", "amount": "1000"}' --accountId <your-account.testnet>
```

#### Transferring Tokens
```bash
near call <your-account.testnet> ft_transfer '{"receiver_id": "receiver.testnet", "amount": "10"}' --accountId <your-account.testnet> --depositYocto 1
```

#### Checking Balance
```bash
near view <your-account.testnet> ft_balance_of '{"account_id": "receiver.testnet"}'
```

## **Development & Testing**
### Running Tests
```bash
npm test
```

---

## **Standards**
- [NEP-141 Fungible Token Standard](https://nomicon.io/Standards/Tokens/FungibleTokenCore.html)

