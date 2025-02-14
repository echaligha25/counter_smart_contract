# Counter Smart Contract

This project demonstrates how to build and deploy a smart contract on StarkNet using the `starknet-dev` container image. Below are the setup instructions and key commands to get started.

---

## Prerequisites

1. **Git:** Ensure Git is installed on your system.
2. **Docker:** Make sure Docker is installed and running.
3. **Devcontainer Setup:**
   - The project uses the `starknetfoundation/starknet-dev:latest` image.
   - Ensure your development environment supports devcontainers (e.g., VS Code with the Remote - Containers extension).

---

## Getting Started

### Clone the Repository
```bash
git clone https://github.com/starknet-edu/basecamp11-app.git
cd basecamp11-app
```

### Initialize the Devcontainer
1. Open the project in VS Code.
2. When prompted, reopen the project in the devcontainer.

---

## StarkNet Setup

### Create a Keystore
Generate a new keystore file to securely store your private key:
```bash
starkli signer keystore new keystore.json
```

### Initialize Your Account
Create a new StarkNet account:
```bash
starkli account oz init account.json --keystore keystore.json
```

### Deploy Your Account
Deploy the account to the StarkNet network:
```bash
starkli account deploy account.json --keystore keystore.json
```

---

## Deploying the Smart Contract

### Declare the Contract
Declare your smart contract class:
```bash
starkli declare target/dev/sn_workshop_Counter.contract_class.json --account account.json --keystore keystore.json
```

### Deploy the Contract
Deploy the declared contract to the StarkNet network. Replace placeholders with actual values:
```bash
starkli deploy Contract-Class-Hash InitialNumber DestinationAccount --account account.json --keystore keystore.json
```
#### Example:
```bash
starkli deploy 0x059008e773455069448845ec2a7557f8c8fe9dc94afaff13fd90865f1aaa17c4 4 0x045f9be2a7c7c8e2af0db69305fa175d9f37ed2be5356d63897b670bf0e04a3a --account account.json --keystore keystore.json
```

---

## Resources
- [Cairo Lang - Contract Events](https://book.cairo-lang.org/ch101-03-contract-events.html)
- [StarkNet Documentation](https://docs.starknet.io)
- [StarkNet by Example](https://starknet-by-example.voyager.online/applications/simple_vault)
- [OpenZeppelin Cairo Contracts](https://docs.openzeppelin.com/contracts-cairo/0.20.0/access)
- [StarkLi - Accounts Guide](https://book.starkli.rs/accounts)
- [Foundry StarkNet Integration](https://foundry-rs.github.io/starknet-foundry/)

---

## Notes
- Ensure you have sufficient StarkNet testnet tokens for deploying contracts and accounts.
- Replace placeholder values in commands (e.g., `Contract-Class-Hash`, `InitialNumber`, `DestinationAccount`) with actual values based on your contract and deployment requirements.

