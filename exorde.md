---
description: Guide Exorde Testnet
---

# Exorde

​[​<img src=".gitbook/assets/twitter-removebg-preview.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg) [Twitter BeritaCryptoo](https://twitter.com/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png) [Telegram BeritaCryptoo](https://t.me/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png) [Discord BeritaCryptoo](https://discord.gg/beritacryptoonode)

## Cara Install menggunakan Docker

#### Install Docker

```
sudo apt update -y && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt install docker-ce
```

#### Download Bahan

```
git clone https://github.com/exorde-labs/ExordeModuleCLI.git
```

#### Install

```
cd ExordeModuleCLI
docker build -t exorde-cli . 
```

Tunggu sampai selesai

#### Jalankan Screen dan mulai Node

```
docker run -d --restart unless-stopped --pull always --name exorde-cli rg.fr-par.scw.cloud/exorde-labs/exorde-cli -m Address0x -l 2
```

```
docker logs -f exorde-cli
```

Ganti `Address0x` dengan address metamask mu(WalletBaru)

Contoh:

> docker run -d --restart unless-stopped --pull always --name exorde-cli rg.fr-par.scw.cloud/exorde-labs/exorde-cli -m 0x0000000000000000000000000000000000DEAD -l 2

#### Tonton

Di tunggu bisa, close juga bisa…. Gunakan `CTRL+C` untuk close, untuk cek kembali gunakan

```
docker logs -f exorde-cli
```
