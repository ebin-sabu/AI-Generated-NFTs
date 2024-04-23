# AI-Generated NFT Minting Platform
This project uses Artificial Intelligence to create unique NFTs (Non-Fungible Tokens). Allowing users to connect their Ethereum wallets, generate images based on AI-driven prompts, and mint these images as NFTs directly on the Ethereum blockchain.

<p align="center">
  <img width="370" height="300" alt="Screenshot 2024-04-22 at 16 50 44" src="https://github.com/ebin-sabu/AI-Generated-NFTs/assets/49438210/895f67b7-4081-4a52-82c3-6aecee8798c1">
  <img width="370" height="300" alt="Screenshot 2024-04-22 at 16 51 10" src="https://github.com/ebin-sabu/AI-Generated-NFTs/assets/49438210/6c00f0fc-151b-4adf-bad6-87035aa76afe">
  <img width="370" height="300" alt="Screenshot 2024-04-22 at 16 49 52" src="https://github.com/ebin-sabu/AI-Generated-NFTs/assets/49438210/c8169060-836e-405c-8536-d0ceccdbb211">
</p>

## Key Features

#### Wallet Connectivity: 
Seamlessly connect to Ethereum wallets like MetaMask to authenticate and interact with the Ethereum blockchain, done using thirdWeb API

#### AI-Powered Image Generation: 
Utilize Open AI's Dall-e model to generate digital art based on user input prompts. Each image is unique, offering users a personalized experience.

#### NFT Minting: 
Mint the generated images as NFTs on the Ethereum blockchain (Sepolia Testnet), allowing users to own, trade, or collect digital artworks.

#### Smart Contract Interaction: 
Interact directly with smart contracts for minting and managing NFTs, using thirdWeb and ECR721 standard

#### Responsive UI: 
A user-friendly and responsive web interface that provides an easy and efficient user experience across various devices.


## Getting Started

After cloning this repo, Install the required dependencies:

```bash
npm install
```

Then, run the development server by:

```bash
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.


## Learn More

### Required Variables:

ENCRYPTION_PASSWORD -	Provide a string to encrypt sensitive data stored in DB. Do not change this value or encrypted data will be inaccessible.

THIRDWEB_SECRET_KEY -	A thirdweb secret key created on the API Keys page.

BACKEND_WALLET_ADDRESS -	The wallet address that will configure Engine from the thirdweb dashboard. You will be able to add other admins later.

POSTGRES_CONNECTION_URL -	Postgres connection string: postgresql://[user[:password]@][host][:port][/dbname][?param1=value1&...] .

ENGINE_URL - Default set as (https://localhost:3005).

NEXT_PUBLIC_CLIENT_ID - Contract ID from thirdWeb.

OPENAI_SECRET_KEY - Use open AI to get this.


### Self-Host Instructions:

#### Requirements:
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





