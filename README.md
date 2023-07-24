# Alien888 NFTs

#### deploy a contract

```shell
npx hardhat run scripts/deploy.ts
```


#### deploy a subgraph

Create a subgraph called `my_contract_123` at `https://thegraph.com/studio/subgraph/`
```
graph auth --studio <deploy_key>

graph init --contract-name MyContract123 --index-events --studio \
  --from-contract <contract_addrees> \
  --abi abi.json \
  --network arbitrum-one \
  my_contract_123
```

Then deploy it

```
cd my_contract_123
yarn deploy
```

Done!

#### Note that ...

...either the name of a subgraph created in Studio - `slug` - must match the one specified in `graph init...`:

```
my_contract_123 == my_contract_123
```

or a slug must be specified explicitly:

```
graph deploy --studio <subgraph-slug>
```

#### Examples

Install dependencies
```
brew install node
npm i
```

Fill in the `.env` file with the real data
```
cp .env.example
vim .env
```

Run it
```
node ex1.js
```

#### Faucets Ethereum Sepolia:
  * https://www.infura.io/faucet/sepolia
  * https://faucet.quicknode.com/ethereum/sepolia
