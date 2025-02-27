## Network Endpoints {: #network-endpoints }

Moonriver has two types of endpoints available for users to connect to: one for HTTPS and one for WSS. 

If you're looking for your own endpoints suitable for production use, you can check out the [Endpoint Providers](/builders/get-started/endpoints/#endpoint-providers){target=_blank} section of our documentation. Otherwise, to get started quickly you can use one of the following public HTTPS or WSS endpoints:

--8<-- 'text/endpoints/moonriver.md'

## Quick Start {: #quick-start } 

Before getting started, make sure you've retrieved your own endpoint and API key from one of the custom [Endpoint Providers](/builders/get-started/endpoints/){target=_blank}. Then for the [Web3.js library](/builders/build/eth-api/libraries/web3js){target=_blank}, you can create a local Web3 instance and set the provider to connect to Moonriver (both HTTP and WS are supported):

```js
const Web3 = require('web3'); // Load Web3 library
.
.
.
// Create local Web3 instance - set Moonriver as provider
const web3 = new Web3("RPC-API-ENDPOINT-HERE"); // Insert your RPC URL here
```

For the [Ethers.js library](/builders/build/eth-api/libraries/ethersjs){target=_blank}, define the provider by using `ethers.JsonRpcProvider(providerURL, {object})` and setting the provider URL to Moonriver:

```js
const ethers = require('ethers'); // Load Ethers library

const providerURL = "RPC-API-ENDPOINT-HERE"; // Insert your RPC URL here

// Define provider
const provider = new ethers.JsonRpcProvider(providerURL, {
    chainId: 1285,
    name: 'moonriver'
});
```

Any Ethereum wallet should be able to generate a valid address for Moonbeam (for example, [MetaMask](https://metamask.io/){target=_blank}).

## Chain ID {: #chain-id } 

Moonriver chain ID is: `1285`, or `0x505` in hex.
