# Simple domains registration on Polygon


## Initial project config
```bash
npm init -y

# Hardhat - Ethereum development environment
npm install --save-dev hardhat

# waffle - Advanced framework for testing smart contracts
npm install --save-dev @nomiclabs/hardhat-waffle ethereum-waffle chai 

# A complete Ethereum wallet implementation and utilities in JavaScript (and TypeScript)
npm install --save-dev @nomiclabs/hardhat-ethers ethers

# includes the most used implementations of ERC standards
npm install @openzeppelin/contracts

# the accounts tasks is not included in the version 2.10.2. Add the following in your hardhat.config.js
# task("accounts", "Prints the list of accounts", async () => {
#   const accounts = await ethers.getSigners();

#   for (const account of accounts) {
#     console.log(account.address);
#   }
# });
npx hardhat accounts

# compiles and tests the sample contract to see if everything is working
npx hardhat compile
```

### Advertência
https://hardhat.org/hardhat-chai-matchers/docs/migrate-from-waffle

### Create run.js files in scripts folder to run and debug contracts
```hre``` is an object containing all the functionality that Hardhat exposes when running a task, test or script.
```bash
npx hardhat run scripts/run.js
```


## Implementations notes

ERC721 token with storage based token URI management
```javascript
import "@openzeppelin/contracts/token/ERC721/extensions/ERC721URIStorage.sol";
```

