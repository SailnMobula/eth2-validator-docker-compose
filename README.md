# Setup a ETH2 Validator

clone the repo and change into

```
git clone https://github.com/kramerjul/eth2-validator-docker-compose.git
```

Change into the repo and create a environment variable `PROJECT_PATH`

```
cd eth2-validator-docker-compose/
PROJECT_PATH=${PWD}
```

## Create all folders

Change the directory to the deployment-folder

```
cd deployment-pyrmont/
```

Let's create a environment variable `DEPLOYMENT_PATH`

```
DEPLOYMENT_PATH=${PWD}
```

First create all folders

```shell
mkdir -p ${DEPLOYMENT_PATH}/data/goethereum
mkdir -p ${DEPLOYMENT_PATH}/data/grafana
mkdir -p ${DEPLOYMENT_PATH}/data/prometheus
mkdir -p ${DEPLOYMENT_PATH}/data/prysm/beaconchain
mkdir -p ${DEPLOYMENT_PATH}/data/prysm/validator/passwords
mkdir -p ${DEPLOYMENT_PATH}/data/prysm/validator/wallets
mkdir -p ${DEPLOYMENT_PATH}/data/keys
```

Let's choose a password in order to secure your wallet which will be created later on

```
echo <YOUR_WALLET_PASSWORD> >> ${DEPLOYMENT_PATH}/data/prysm/validator/password/wallet-password
```

## Get Goerli

We will need to deposit 32 GörliETH to register a validator. You can request GörliETH [here](https://faucet.goerli.mudit.blog/). I recommend setting up a Metamask account before.

## Generate Keys

First install the official `eth2.0-deposit-cli` in order to generate your keys
```
cd ${PROJECT_PATH}
curl -LO https://github.com/ethereum/eth2.0-deposit-cli/releases/download/v1.1.0/eth2deposit-cli-ed5a6d3-linux-amd64.tar.gz
tar -xzf eth2deposit-cli-ed5a6d3-linux-amd64.tar.gz 
rm -f eth2deposit-cli-ed5a6d3-linux-amd64.tar.gz 
cd eth2deposit-cli-ed5a6d3-linux-amd64/
```

Generate new validator keys. Make sure you use the correct chain. For testnet `pyrmont`, for mainnet `mainnet`
```
./deposit new-mnemonic --num_validators 1 --chain pyrmont
```

Copy your keys to the deployment path
```
cp -r <YOUR_KEYS_PATH/validator_keys> ${DEPLOYMENT_PATH}/data/keys/
```

## Register your wallet

visit the [pyrmont-launchpad](https://pyrmont.launchpad.ethereum.org/) and follow the instructions to register a validator. After that import the account with

```
sudo docker-compose -f docker-compose.create-account.yml run validator-import-launchpad
```

You can check your imported account by running

```
sudo docker-compose -f docker-compose.create-account.yml run validator-list-accounts
```

## Add certs for nginx

Add your certs to the folder `./config/nginx/certs`

Change the certs name in the config file `./config/nginx/nginx.conf`

## Start everything up

Start your eth1-client, beacon-chain-client, validator, prometheus and grafana with

```
sudo docker-compose up -d
```
