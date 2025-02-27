# Based Starter Template for Building UNSTOPPABLE  EVM Dapps

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

A robust template for building decentralized frontends that interact with Base, Ethereum, and other EVM chains, with permanent deployment capabilities on Arweave via Arlink.

## 🎉 Features

### Core Technologies
- **React** - A JavaScript library for building user interfaces.
- **Vite** - A fast, modern frontend build tool.
- **TypeScript** - A type-safe development language.
- **Tailwind CSS** - A utility-first CSS framework.
- **shadcn presetup** - The template is compatible with shadcn and V0 out of the box.

### Web3 Integration
- **wagmi** - React Hooks for Ethereum.
- **RainbowKit** - Wallet connection management.
- **ethers.js** - Ethereum interactions.
- **Base Chain Support** - Optimized for Base with easy configuration for other EVM chains.

### Decentralized Deployment
- **ArLink Support** - Simplified deployment to Arweave.

## ⚙️ Prerequisites

- Node.js (version 16 or above).
- Yarn (package manager).
- An Arweave wallet/keyfile for deployment.
- Test ETH on your preferred network (Base Goerli for testing).

## 🔗 Chain Configuration

### Supported Networks
- Base (Mainnet & Testnet).
- Ethereum (Mainnet & Goerli).
- Other EVM-compatible chains.

To add or modify chains:

```typescript
// Update chain configuration in wagmi config
const chains = [base, baseGoerli, mainnet, goerli];
```

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone [your-repo-url]
   ```

2. Install dependencies:
   ```bash
   yarn
   ```

3. Configure your environment:
   ```bash
   cp .env.example .env
   ```
   Add your:
   - RPC URLs
   - Chain IDs
   - Arweave keyfile location
   - Other API keys

4. Start development:
   ```bash
   yarn dev
   ```

## 📜 Available Scripts

- `yarn dev` - Start the development server.
- `yarn build` - Build production-ready code.
- `yarn deploy:arweave` - Deploy to Arweave via ArLink.

## 🌐 Deployment

### Arweave Deployment (via ArLink)

Benefits:
- Permanent, immutable storage.
- One-click hosting.
- True decentralization.
- Content-addressed storage.
- CI/CD integration.
- ARNS integration for deploying your apps with human-readable names.

Steps:
1. Clone this template from the ArLink template marketplace.
2. Clone locally.
3. Commit your changes.
4. Push to the main branch to update your changes on the permaweb.

5. Build your project:
   ```bash
   yarn build
   ```

6. Deploy:
   ```bash
   yarn deploy:arweave
   ```

## 📂 Project Structure

```
project-root/
  ├── src/
  │   ├── components/     # React components
  │   ├── contracts/      # Contract ABIs and addresses
  │   ├── hooks/          # Custom Web3 hooks
  │   ├── lib/            # Utilities and configurations
  │   │   ├── chains.ts   # Chain configurations
  │   │   └── wagmi.ts    # wagmi client setup
  │   └── pages/          # Application pages
  └── vite.config.ts      # Vite configuration
```

## ⚡ Development Constraints for Arweave Compatibility

To ensure your site runs smoothly on Arweave, consider the following constraints:

- **Client-Side Rendering**: Ensure that your application is fully client-side rendered. Arweave does not support server-side rendering, so all necessary data must be fetched and rendered on the client side.
- **Static Assets**: Use static assets that can be served directly from Arweave. Avoid dynamic content that requires server-side processing.
- **Bundle Size**: Optimize your bundle size to reduce deployment costs and improve loading times. Use code splitting and lazy loading where possible.
- **Error Handling**: Implement robust error handling to manage potential issues with network requests or wallet connections.
- **Testing**: Thoroughly test your application on the Base Goerli test network before deploying to ensure compatibility and performance.

## 🔒 Security Best Practices

- Environment variable management.
- Private key security.
- RPC endpoint security.
- Contract interaction safety.

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details.
