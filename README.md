# NFTseum - Revolutionizing Music NFTs

Welcome to NFTseum, where music NFTs take center stage in a revolutionary new way to experience and collect music. This platform empowers artists to directly connect with enthusiasts, allowing for the seamless creation, sale, and ownership transfer of music as a valuable asset. Here's a comprehensive guide to navigating and contributing to the NFTseum project.

## Contract Details

Our smart contract, written in Solidity and deployed on the Polygon Mumbai network, utilizes the ERC-721 protocol to mint token URIs for music art uploaded to IPFS. To deploy your own contract, follow these steps:

1. Add Polygon Mumbai to your wallet.
2. Obtain a polygonscan API key.
3. Navigate to `/src/Contracts` and refer to the `env_sample` file to create your environment file with the required fields.
4. Run `npm install` or `yarn install` to install dependencies.
5. Compile using `npx hardhat compile`.
6. Deploy with `npx hardhat run scripts/deploy.js --network polygon_mumbai`.

Remember to save the contract address for frontend fetching.

## Integration Details

1. **Frontend UI**: Built with ReactJS and styled using TailwindCSS, MUI, and styled components modules.
2. **Media Upload to IPFS**: Made possible by the NFT.STORAGE API for uploading and obtaining CID.
3. **Blockchain Integration**: Uses Alchemy endpoint RPC to connect the app to the deployed smart contract.
4. **Firebase Backend**: Utilizes Google Firebase Firestore for smooth off-chain storage of user and NFT data.

To integrate Firebase backend:

- Start a new Firebase server.
- Create a new web app and configure FirebaseConfig.js in `src/BackendConfig` accordingly.
- Add collections: users, artists, happy, sad, angry (expand based on moods).

To integrate blockchain:

- Obtain an API key from NFT.STORAGE.
- Get an API key from Alchemy with the Polygon network RPC.
- Add all API keys and the contract address to the env file in the root folder.


## Running the Application

Navigate to the root folder in the terminal and run:

```bash
npm install
npm run start
```

Explore the innovative world of NFTseum at [www.nftseum.com](www.nftseum.com). Join us on this journey where artists and enthusiasts converge to redefine the landscape of music ownership and consumption.