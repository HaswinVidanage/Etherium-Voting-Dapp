# Etherium Voting Dapp

A Decentralized Voting Application made using etherium and web 3.0

## Getting Started

Clone the repo and run the following on terminal.
```
> cd Etherium-Voting-Dapp
> npm install
> node_modules/ethereumjs-testrpc/build/cli.node.js
```

```
> node
> Web3 = require('web3')
> web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
> code = fs.readFileSync('Voting.sol').toString()
> solc = require('solc')
> compiledCode = solc.compile(code)
> abiDefinition = JSON.parse(compiledCode.contracts[':Voting'].interface)
> VotingContract = web3.eth.contract(abiDefinition)
> byteCode = compiledCode.contracts[':Voting'].bytecode
> deployedContract = VotingContract.new(['Rama','Nick','Jose'],{data: byteCode, from: web3.eth.accounts[0], gas: 4700000})
> deployedContract.address
> contractInstance = VotingContract.at(deployedContract.address)
```

Copy the contract address and assign the value to contractAddress variable in index.js
```
> deployedContract.address
```

## Running

Run index.html on a browser and enter a name and vote.

## Credits
Based on the work by [maheshmurthy](https://gist.github.com/maheshmurthy)
