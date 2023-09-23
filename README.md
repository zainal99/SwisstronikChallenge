# Swisstronik Challenge ETH getStorage

In this project, there are sample contracts, tests, and scripts that deploy contracts, as well as the Swisstronik blockchain network. This case demonstrates the basic usage of Hardhat.

## Task

Make a JSON RPC call using eth_getStorageAt() to get the first storage variable (slot #0) of any deployed smart contract and explain what is the retrieved value or if there is any difference with other blockchains when using this RPC method.

## Usage

Installation Package

```
npm install
```

### Network: Swisstronik

#### `Request`

```shell
npx hardhat run scripts/getStorage.js --network swisstronik
```

#### `Response`

```shell
{
  contract: '0xf84Df872D385997aBc28E3f07A2E3cd707c9698a',
  slotNumber: 0,
  rpcURL: 'https://json-rpc.testnet.swisstronik.com/'
}

Response:
Storage Value at Slot 0: 0x0xc73e7f645a2bf1365a0903afa03a2cb5029ba989df7844b0fe7751b1ba918ea4
```

### Network: Ethereum Sepolia

#### `Request`

```shell
npx hardhat run scripts/getStorage.js --network sepolia
```

#### `Response`

```shell
{
  contract: '0xf84Df872D385997aBc28E3f07A2E3cd707c9698a',
  slotNumber: 0,
  rpcURL: 'https://rpc.sepolia.org'
}

Response:
Storage Value at Slot 0: 0x0x0000000000000000000000000000000000000000000000000000000000000000
```

### Network: Polygon Mumbai

#### `Request`

```shell
npx hardhat run scripts/getStorage.js --network mumbai
```

#### `Response`

```shell
{
  contract: '0xf84Df872D385997aBc28E3f07A2E3cd707c9698a',
  slotNumber: 0,
  rpcURL: 'https://polygon-mumbai.blockpi.network/v1/rpc/public'
}

Response:
Storage Value at Slot 0: 0x0x0000000000000000000000000000000000000000000000000000000000000000
```

## Smart Contract

```
0xf84Df872D385997aBc28E3f07A2E3cd707c9698a 
```

## Conclusion

Here I use the ethers v6 package. and the difference between the Ethers v5 and v6 packages is in the Get Storage Function

`Ethers v5`

```
getStorageAt()
```

`Ethers v6`

```
getStorage()
```
