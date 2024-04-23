# AI-Generated NFT Minting Platform
This project use Artificial Intelligence to create unique NFTs (Non-Fungible Tokens). Allowing Users to connect their Ethereum wallets, generate images based on AI-driven prompts, and mint these images as NFTs directly on the Ethereum blockchain.

## Key Features

##### Wallet Connectivity: 
Seamlessly connect to Ethereum wallets like MetaMask to authenticate and interact with the Ethereum blockchain, done using thirdWeb API

##### AI-Powered Image Generation: 
Utilize Open AI's Dall-e model to generate digital art based on user input prompts. With each image being unique, offering users a personalized experience.

##### NFT Minting: 
Mint the generated images as NFTs on the Ethereum blockchain (Sepolia Testnet), allowing users to own, trade, or collect digital artworks.

##### Smart Contract Interaction: 
Interact directly with smart contracts for minting and managing NFTs, using thirdweb and ECR721 standard

#####  Responsive UI: 
A user-friendly and responsive web interface that provides an easy and efficient user experience across various devices.


## Getting Started

After cloning this repo, Install required dependecies:

```bash
npm install
```

Then, run development server by:

```bash
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.


## Learn More

### Self-Host Instructions:

##### Requirements:
Docker
A thirdweb secret key from the API Keys page
PostgresDB (version 14+)

```bash
docker run -p 5432:5432 -e POSTGRES_PASSWORD=postgres -d postgres
```

```bash
docker run \
  -e ENCRYPTION_PASSWORD="<encryption_password>" \
  -e THIRDWEB_API_SECRET_KEY="<thirdweb_secret_key>" \
  -e ADMIN_WALLET_ADDRESS="<admin_wallet_address>" \
  -e POSTGRES_CONNECTION_URL="postgresql://postgres:postgres@host.docker.internal:5432/postgres?sslmode=disable" \
  -e ENABLE_HTTPS=true \
  -p 3005:3005 \
  --pull=always \
  --cpus="0.5" \
  thirdweb/engine:latest
```





