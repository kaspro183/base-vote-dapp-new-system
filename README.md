# Base Voting dApp — Solidity + Hardhat + Frontend

Projet prêt à publier sur GitHub pour montrer de l'activité **Web3/crypto** (parfait pour Talent Protocol).
- Réseau cible : **Base Sepolia** (testnet)
- Contrat : `Poll.sol` (vote A/B, une voix par adresse)
- Frontend simple (HTML + JS + ethers.js) pour voter via MetaMask

> Pas besoin de déployer pour Talent Protocol — **les commits GitHub suffisent**.  
> Pour tester la dApp, déployez sur **Base Sepolia** puis configurez `frontend/app.js`.

## Structure
```
base-vote-dapp/
├── contracts/Poll.sol
├── scripts/deploy.js
├── hardhat.config.js
├── package.json
└── frontend/
    ├── index.html
    └── app.js
```

## Déploiement (optionnel)
```bash
npm i
npx hardhat compile

# Variables d'env pour Base Sepolia
# export BASE_SEPOLIA_RPC="https://sepolia.base.org"
# export PRIVATE_KEY="0x..."
npx hardhat run scripts/deploy.js --network base_sepolia
```

## Frontend (après déploiement)
- Ouvrez `frontend/app.js` et remplacez :
  - `const POLL_ADDRESS = "0xYourPoll";`
- Ouvrez `frontend/index.html` (MetaMask + réseau **Base Sepolia**).
