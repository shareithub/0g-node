# 0G DA CLIENT TUTORIAL 

Dont forget to Subscribe my Channel :

[ TELEGRAM CHANNEL](https://t.me/SHAREITHUB_COM)

[YOUTUBE CHANNEL](https://www.youtube.com/channel/UCUvH2S-T6T_hc7DjxhVd28A/)

---------------------------------------------------------------------------

[ TUTORIAL BY VIDEO ](https)

# Tutorial by Text :

Install git :
```
sudo apt install git -y
```
Install Docker.io :
```
sudo apt install docker.io -y
```
Start & Enable Docker :
```
sudo systemctl start docker
sudo systemctl enable docker
```
Check Docker Status :
```
sudo systemctl status docker
```

# Install NODE DA-Client :

Git clone DA-Client repository :
```
git clone https://github.com/0glabs/0g-da-client.git
```
Go to Folder & Build Docker Image :
```
cd 0g-da-client
docker build -t 0g-da-client -f combined.Dockerfile .
```
Create File "envfile.env" :
```
nano envfile.env
```
Copy & change your private keys in text ("YOUR_PRIVATE_KEY") :
```
# envfile.env
COMBINED_SERVER_CHAIN_RPC=https://evmrpc-testnet.0g.ai
COMBINED_SERVER_PRIVATE_KEY=YOUR_PRIVATE_KEY
ENTRANCE_CONTRACT_ADDR=0x857C0A28A8634614BB2C96039Cf4a20AFF709Aa9

COMBINED_SERVER_RECEIPT_POLLING_ROUNDS=180
COMBINED_SERVER_RECEIPT_POLLING_INTERVAL=1s
COMBINED_SERVER_TX_GAS_LIMIT=2000000
COMBINED_SERVER_USE_MEMORY_DB=true
COMBINED_SERVER_KV_DB_PATH=/runtime/
COMBINED_SERVER_TimeToExpire=2592000
DISPERSER_SERVER_GRPC_PORT=51001
BATCHER_DASIGNERS_CONTRACT_ADDRESS=0x0000000000000000000000000000000000001000
BATCHER_FINALIZER_INTERVAL=20s
BATCHER_CONFIRMER_NUM=3
BATCHER_MAX_NUM_RETRIES_PER_BLOB=3
BATCHER_FINALIZED_BLOCK_COUNT=50
BATCHER_BATCH_SIZE_LIMIT=500
BATCHER_ENCODING_INTERVAL=3s
BATCHER_ENCODING_REQUEST_QUEUE_SIZE=1
BATCHER_PULL_INTERVAL=10s
BATCHER_SIGNING_INTERVAL=3s
BATCHER_SIGNED_PULL_INTERVAL=20s
BATCHER_EXPIRATION_POLL_INTERVAL=3600
BATCHER_ENCODER_ADDRESS=DA_ENCODER_SERVER
BATCHER_ENCODING_TIMEOUT=300s
BATCHER_SIGNING_TIMEOUT=60s
BATCHER_CHAIN_READ_TIMEOUT=12s
BATCHER_CHAIN_WRITE_TIMEOUT=13s
```
SAVE FILE : CTRL + X + Y. Enter

After done, u can start node  :
```
docker run -d --env-file envfile.env --name 0g-da-client -v ./run:/runtime -p 51001:51001 0g-da-client combined 
```

# DONE
Don't forget Subscribe , Like & Share
# SHARE IT HUB















