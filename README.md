[![Docker](https://github.com/commoodor/hellminer-docker/actions/workflows/docker-publish.yml/badge.svg?branch=latest)](https://github.com/commoodor/hellminer-docker/actions/workflows/docker-publish.yml)
# Docker-Hellminer
Docker containing Hellminer v0.59.1

More documentation on Hellminer v0.59.1: https://github.com/hellcatz/hminer

## Here is a example to get going with a server using compose. ##
~~~
version: '3.8'

services:
  hellminer_saturn:
    container_name: hellminer_saturn
    image: commoodor/hellminer-docker
    restart: unless-stopped
    tty: true
    mem_limit: 1g
    environment:
      POOL_ADDRESS: stratum+ssl://sg.vipor.net:5140
      WALLET_USER: RRmpZ1tajCXVG9999LWUD4CPVyZvjpe3iZ
      WORKER: Saturn
      PASSWORD: x
      EXTRAS:
    logging:
      driver: "json-file"
      options:
        max-size: "10m"
        max-file: "3"
~~~

| ** Variable name ** | **Description** | **Value  example** |
|---|---|---|
| POOL_ADDRESS | The address on the pool you want to mine on | stratum+ssl://ap.luckpool.net:3956#xnsub |
| WALLET_USER | This is ussally used as a user field or a wallet address field | RRmpZ1tajCXVG9999LWUD4CPVyZvjpe3iZ |
| WORKER | Your worker name | Saturn |
| PASSWORD | This is the password field | x |
| EXTRAS |  This is a field use to extra parameters | - |



Support Us:

BTC : bc1q3m9qxtaqzhzk0ay6e6dmxmz439n4f73zz0unqp

ETH : 0x37A8997fBBa95cE12553745E2d6BA4F9Ae5Caa84

Doge : D5CiFXE5PvLn5fQKjCuovecExSNjGct5UU
