## Octra-Labs
Octra is a decentralized general purpose peer-to-peer network that allows anyone to securely store and process data using Fully Homomorphic Encryption (FHE). It addresses a simple problem: providing an open and neutral platform for anyone to build robust ecosystems of decentralized applications, based on the principles of confidential isolated processing of numeric data, while retaining access control to said data. Like any other blockchain it is cryptographically secure and acts as a system to process transactions in a distributed environment without central authority. The core difference that allows confidentiality-preserving operations of arbitrary complexity lies in the absence of the need to decrypt raw data to perform these operations, logic or arithmetic, due to innate features of FHE.

## Installation on Linux
1. Install bun
```
curl -fsSL https://bun.sh/install | bash
exec $SHELL
bun --version
```

2. Setup Wallet Generator
```
sudo apt update && sudo apt install ufw -y
sudo ufw allow 8888
```
```
git clone https://github.com/octra-labs/wallet-gen
cd wallet-gen
bun install
bun run build
```
3. Run
```
bun start
```

- A popup window will show, click generate wallet
- Save all details (phrase,address,private key and public key)

4. Request Faucet
https://faucet.octra.network/

## Octra Terminal Client
1. Installation
```
git clone https://github.com/octra-labs/octra_pre_client.git
cd octra_pre_client
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp wallet.json.example wallet.json
```

2. Open wallet.json
```
nano wallet.json
```

3. Edit "priv" and "addr" section with your wallet data
```json
{
  "priv": "private-key-here",
  "addr": "octxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
  "rpc": "https://octra.network"
}
```

4. Run
```
./run.sh
```

- Now you can use it to show your account balances, tx history, and send one or multi tx.



