services:
  celestia-server:
    image: ghcr.io/celestiaorg/nitro-das-celestia:v0.5.2
    container_name: celestia-server
    entrypoint:
      - /bin/celestia-server
      - --celestia.namespace-id
      - "00000d048007a33abfeb"
      - --rpc-addr
      - "0.0.0.0"
      - --rpc-port
      - "26657"
      - --celestia.rpc
      - "CELESTIA_ENDPOINT"
      - --log-level
      - "DEBUG"
    ports:
      - "1317:1317"
      - "9090:9090"
      - "26657:26657" # Celestia RPC Port
      - "1095:1095"
      - "8080:8080"
