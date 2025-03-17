# Veltis Frontend

Frontend application for Veltis - Biotech IP Tokenization Platform

## Overview

This repository contains the frontend code for the Veltis platform, which enables users to create, fractionalize, list, and trade IP NFTs (Intellectual Property Non-Fungible Tokens) in a decentralized marketplace.

## Tech Stack

- React with TypeScript
- Vite
- Tailwind CSS
- Clerk for authentication
- Ethers.js for blockchain interaction
- Web3Modal for wallet connection

## Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- A Web3 wallet like MetaMask

## Development Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Veltiscapital/veltis-frontend.git
   cd veltis-frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env.local` file with the following environment variables:
   ```
   VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   VITE_NFT_STORAGE_API_KEY=your_nft_storage_api_key
   VITE_BLOCKCHAIN_NETWORK=polygon-amoy
   VITE_IP_NFT_REGISTRY_CONTRACT=your_ip_nft_registry_contract_address
   VITE_SIMPLE_IP_NFT_REGISTRY_CONTRACT=your_simple_ip_nft_registry_contract_address
   VITE_FRACTIONALIZATION_FACTORY_CONTRACT=your_fractionalization_factory_contract_address
   VITE_POLYGON_AMOY_RPC_URL=your_polygon_amoy_rpc_url
   VITE_CHAIN_ID=80002
   VITE_NETWORK_NAME=Polygon Amoy Testnet
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Open your browser and navigate to `http://localhost:3000`

## Building for Production

```bash
npm run build
```

The build artifacts will be stored in the `dist/` directory.

## Deployment

The frontend is deployed to Vercel. Use the `deploy-to-vercel.sh` script to deploy:

```bash
./deploy-to-vercel.sh
```

### Deployment Script

The deployment script performs the following actions:

1. Checks for required environment variables
2. Creates necessary configuration files
3. Builds the application
4. Deploys to Vercel

## Troubleshooting

If you encounter a blank page after deployment, try the following:

1. Clear your browser cache
2. Check browser console for errors
3. Verify that all environment variables are set correctly in Vercel
4. Ensure the routing configuration is correct

## Project Structure

```
├── public/             # Static assets
├── src/
│   ├── components/     # React components
│   ├── contexts/       # React contexts
│   ├── hooks/          # Custom React hooks
│   ├── layouts/        # Page layouts
│   ├── lib/            # Utility libraries
│   ├── pages/          # Page components
│   ├── types/          # TypeScript type definitions
│   ├── utils/          # Utility functions
│   ├── App.tsx         # Main App component
│   ├── main.tsx        # Entry point
│   └── routes.tsx      # Route definitions
├── .env.example        # Example environment variables
├── index.html          # HTML template
├── package.json        # Project dependencies
├── tsconfig.json       # TypeScript configuration
├── vite.config.ts      # Vite configuration
└── vercel.json         # Vercel configuration
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.