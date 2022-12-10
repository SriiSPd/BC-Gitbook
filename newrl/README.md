---
description: Guide Newrl Mainnet
---

# Newrl



<figure><img src="../.gitbook/assets/NEWWRL.png" alt=""><figcaption></figcaption></figure>

## Setup

#### Shutdown Node Testnet

```
cd ~/newrl-venv/newrl
scripts/kill_server.sh
```

Dan simpan file `.auth.json` di `~/newrl-venv/newrl/data_testnet`\
Selanjutnya hapus directory

```
cd
rm -rf newrl-venv
```

#### Open Port

```
sudo ufw allow ssh && sudo ufw allow 8456 && sudo ufw enable
```

#### Update

```
sudo apt update && sudo apt upgrade -y
```

#### Install Screen

```
sudo apt install -y build-essential libssl-dev libffi-dev git curl screen
```

#### Install Python

```
sudo apt install python3.9
```

#### Install Pip & Python3 venv

```
curl -sSL https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py
sudo apt install python3.9-venv
```

#### Buat Directory Baru dan Aktifkan

```
sudo mkdir newrl-venv
cd newrl-venv
python3.9 -m venv newrl-venv
```

```
source newrl-venv/bin/activate
```

#### Download + Mulai Script

```
git clone https://github.com/newrlfoundation/newrl.git
cd newrl
scripts/install.sh mainnet
```

#### Import Wallet ke VPS

```
cd ~/newrl-venv/newrl/data_mainnet
```

```
nano .auth.json
```

Isi dengan semua data dari wallet testnet lalu save. `CTRL+X` `Y` `Enter`

Format data yang di import harus seperti ini :

> {"public": "fefcdb9c187f241ffbe76ef89ee9ff85dcd6a1ba0ad60dedaeb195d4azzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz", "private": "be46bf4f061d6a6d813005zzzzzzzzzzzzzzzzzzzzzzzzzzz", "address": "0x0000000000000000000000000000000000000DEAD"}

#### Cek untuk memasatikan

```
cd ~/newrl-venv/newrl
python3 scripts/show_wallet.py
```

Ketik mainnet, enter, Y

#### Import ke Web Wallet

* Buka [Wallet Newrl](https://wallet.newrl.net/)
* Jika masih ada wallet testnet nya disana, tidak perlu import lagi. Langsung klik pojok kanan atas dan ganti ke mainnet
* Klik Activate Wallet dan KYC ulang
* Tunggu sampai di acc

### Memulai Node

#### Jalankan Node

```
screen -S newrl
```

```
scripts/start.sh mainnet --fullnode
```

Untuk keluar dari sesi logs tekan `CTRL+A+D`

Untuk kembali cek logs

```
screen -Rd newrl
```

### Staking OG Token

Setelah mendapat 1 OG Token dan 10 Newrl di wallet mainnet, pergi wallet buka Validator Management

Pilih Stake Using My OG Token

Cek kembali di wallet dan tunggu sampai Newrl mulai di produksi

#### Cek Trust Score

```
http://archive1-mainnet.newrl.net:8456/get-incoming-trustscores?dst_wallet_addres
```
