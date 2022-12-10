---
description: Guide Loyal Testnet
---

# Loyal



​[​<img src=".gitbook/assets/twitter-removebg-preview.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg) [Twitter BeritaCryptoo](https://twitter.com/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png) [Telegram BeritaCryptoo](https://t.me/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png) [Discord BeritaCryptoo](https://discord.gg/beritacryptoonode)[​](https://twitter.com/BeritaCryptoo)​

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FbGNwC59ZoICKLkH4frjI%2FqIdvDEqz_400x400.jpg?alt=media&#x26;token=2c39e138-322f-4bb9-aac1-a9b7b7c96d88" alt=""><figcaption></figcaption></figure>

#### Official Link <a href="#official-link" id="official-link"></a>

* ​[Discord](https://discord.gg/Xb5sfGzMwW)​
* ​[Twitter](https://twitter.com/LoyalRewards)​
* ​[Guide](https://docs.joinloyal.io/how-it-works/demo-site)​

​[Explorer](https://ping-pub.joinloyal.io/loyal)​

#### Spesifikasi Minimal <a href="#spesifikasi-minimal" id="spesifikasi-minimal"></a>

* 3x CPU; the higher the clock speed the better
* 4GB of RAM
* 80GB Disk

#### Automatic Setup <a href="#automatic-setup" id="automatic-setup"></a>

```
wget -O loyal.sh https://raw.githubusercontent.com/Megumiiiiii/Loyal-Testnet/main/loyal.sh && chmod +x loyal.sh && ./loyal.sh
```

#### Cek Sync <a href="#cek-sync" id="cek-sync"></a>

```
loyald status 2>&1 | jq .SyncInfo
```

#### Create Wallet <a href="#create-restore-wallet" id="create-restore-wallet"></a>

```
loyald keys add $LYL_WALLET
```

#### &#x20;Restore Wallet <a href="#create-restore-wallet" id="create-restore-wallet"></a>

```
loyald keys add $LYL_WALLET --recover
```

#### List Wallet <a href="#list-wallet" id="list-wallet"></a>

```
loyald keys list
```

#### Export Variable ( Optional ) <a href="#export-variable-optional" id="export-variable-optional"></a>

```
LYL_WALLET_ADDRESS=$(loyald keys show $LYL_WALLET -a)
LYL_VALOPER_ADDRESS=$(loyald keys show $LYL_WALLET --bech val -a)
echo 'export LYL_WALLET_ADDRESS='${LYL_WALLET_ADDRESS} >> $HOME/.bash_profile
echo 'export LYL_VALOPER_ADDRESS='${LYL_VALOPER_ADDRESS} >> $HOME/.bash_profile
source $HOME/.bash_profile
```

#### Cek Saldo <a href="#cek-saldo" id="cek-saldo"></a>

```
loyald query bank balances $LYL_WALLET_ADDRESS
```

#### Faucet <a href="#faucet" id="faucet"></a>

* Ambil di web pake keplr [WEB](https://demo.joinloyal.com/)​
* Register akun baru, masuk ke profil, get 7LYL

#### Create Validator <a href="#create-validator" id="create-validator"></a>

```
loyald tx staking create-validator \
--amount 1000000ulyl \
--from $LYL_WALLET \
--identity ABOGOBOGAAEZAKMI \
--website "https://t.me/BeritaCryptoo" \
--details="Apa yang sedang Anda pikirkan" \
--commission-max-change-rate "0.01" \
--commission-max-rate "0.2" \
--commission-rate "0.08" \
--min-self-delegation "1" \
--pubkey $(loyald tendermint show-validator) \
--moniker $LYL_NODENAME \
--fees 5000ulyl \
--chain-id loyal-1
```

#### ​ <a href="#undefined" id="undefined"></a>

#### Useful Command <a href="#useful-command" id="useful-command"></a>

Identity Validator : \
[https://mirror.xyz/megumii.eth/Rg86BWkUDFYL23lJZYkjTcpaEBsq2keJz\_YfrC1z8sc](https://mirror.xyz/megumii.eth/Rg86BWkUDFYL23lJZYkjTcpaEBsq2keJz\_YfrC1z8sc)

**Seputar Services**

Cek Logs:

```
journalctl -fu loyald -o cat
```

Start Service:

```
systemctl start loyald
```

Stop Service:

```
systemctl stop loyald
```

Restart Service:

```
systemctl restart loyald
```

**Cek Node**

Status Sinkronasi:

```
loyald status 2>&1 | jq .SyncInfo
```

Validator Info:

```
loyald status 2>&1 | jq .ValidatorInfo
```

Node Info:

```
loyald status 2>&1 | jq .NodeInfo
```

Cek Node ID:

```
loyald tendermint show-node-id
```

**Wallet**

Cek List Wallet:

```
loyald keys list
```

Import Wallet:

```
loyald keys add $LYL_WALLET --recover
```

Delete Wallet:

```
loyald keys delete $LYL_WALLET
```

Cek Saldo:

```
loyald query bank balances $LYL_WALLET_ADDRESS
```

Melihat Private Key

```
loyald keys export $LYL_WALLET --unarmored-hex --unsafe
```

Transfer:

```
loyald tx bank send $LYL_WALLET_ADDRESS <TO_WALLET_ADDRESS> 10000000ulyl --fees=5000ulyl
```

**Vote Proposal**

```
loyald tx gov vote 1 yes --from $LYL_WALLET --chain-id=$LYL_ID
```

**Stake, Delegate, Rewards**

Delegate:

```
loyald tx staking delegate $LYL_VALOPER_ADDRESS 10000000ulyl --from=$LYL_WALLET --chain-id=$LYL_ID --gas=auto --fees 5000ulyl
```

Pindah Validator:

```
loyald tx staking redelegate <srcValidatorAddress> <destValidatorAddress> 10000000ulyl --from=$LYL_WALLET --chain-id=$LYL_ID --gas=auto --fees 5000ulyl
```

Withdraw rewards stake + komisi:

```
loyald tx distribution withdraw-all-rewards --from=$LYL_WALLET --chain-id=$LYL_ID --gas=auto --fees 5000ulyl
```

Withdraw rewards stake:

```
loyald tx distribution withdraw-rewards $LYL_VALOPER_ADDRESS --from=$LYL_WALLET --commission --chain-id=$LYL_ID
```

**Merubah Node**

Edit Validator:

```
loyald tx staking edit-validator \
--moniker=NEWNODENAME \
--chain-id=$LYL_ID \
--from=$LYL_WALLET
```

Unjail:

```
loyald tx slashing unjail \
--broadcast-mode=block \
--from=$LYL_WALLET \
--chain-id=$LYL_ID \
--gas=auto \
--fees 250ulyl
```

Delete Node:

```
sudo systemctl stop loyald
sudo systemctl disable loyald
sudo rm /etc/systemd/system/loyald* -rf
sudo rm $(which loyald) -rf
sudo rm $HOME/.loyal* -rf
sudo rm $HOME/loyal* -rf
sed -i '/LYL_/d' ~/.bash_profile
```
