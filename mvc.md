---
description: Guide MVC Testnet
---

# MVC

\
​[​<img src=".gitbook/assets/twitter-removebg-preview.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg) [Twitter BeritaCryptoo](https://twitter.com/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png) [Telegram BeritaCryptoo](https://t.me/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png) [Discord BeritaCryptoo](https://discord.gg/beritacryptoonode)​

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FFINlcLoNQtSeG9YWkNg6%2FK1BG3vs__400x400.jpg?alt=media&#x26;token=179cdd9d-671f-4f72-80ba-067ec23c46ba" alt=""><figcaption></figcaption></figure>

#### Register <a href="#register" id="register"></a>

​[DISINI](https://naire.medium.com/mvc-incentivized-testnet-d7bb23467a3)​

#### Download & Install Bahan Dasar <a href="#download-and-install-bahan-dasar" id="download-and-install-bahan-dasar"></a>

```
wget -O mvc.sh https://raw.githubusercontent.com/Megumiiiiii/MVC/main/mvc.sh && chmod +x mvc.sh && ./mvc.sh
```

#### Edit <a href="#edit" id="edit"></a>

```
nano mvc.conf
```

> Scroll ,cari `rpcuser` dan `rpcpassword` lalu edit dengan nama & passwordmu Seperti ini:

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2F9VYBqdhG2D76riKtGpxk%2FScreenshot_1.png?alt=media&#x26;token=673c5f78-b934-4398-a323-f58d3fa005d6" alt=""><figcaption></figcaption></figure>

> Save menggunakan CTRL+X Y Enter

#### Run <a href="#run" id="run"></a>

Jalankan script

```
./install-node.sh -t --latest
```

Tunggu sampai muncul seperti ini

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FP88PJbZMihZ6cpPK0dVZ%2FScreenshot_2.png?alt=media&#x26;token=94f7ba5a-2feb-4f5b-924e-8aa7979a162b" alt=""><figcaption></figcaption></figure>

**Aktifkan mvc-cli**

```
alias mvc-cli="/root/bin/mvc-cli -conf=/root/mvc.conf"
```

**Mulai Mining**

```
screen -S mvc
```

```
./minerd -a sha256d -o 127.0.0.1:9882 -O akunmu:passwordmu --coinbase-addr=addressmu
```

> akunmu= Akun mu(sesuai di `mvc.conf` )\
> passwordmu= Password mu(sesuai di `mvc.conf`)\
> addressmu= Address dari dashboard yang dibuat di step awal
>
> Contoh:

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2Fvol9SQdK52FIpHfihBoJ%2FScreenshot_4.png?alt=media&#x26;token=4b984de2-1e7f-4610-b397-4bb97133b491" alt=""><figcaption></figcaption></figure>

### OK! <a href="#ok" id="ok"></a>

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FxZToqljk25frc8CRNs1p%2FScreenshot_6.png?alt=media&#x26;token=4686d799-7a36-4634-86bc-f7a2f450f120" alt=""><figcaption></figcaption></figure>

> * Gunakan CTRL+A+D untuk keluar dari sesi logs
> * Untuk cek kembali gunakan

```
screen -Rd mvc
```

#### Delete Node <a href="#delete-node" id="delete-node"></a>

```
alias mvc-cli="/root/bin/mvc-cli -conf=/root/mvc.conf"
mvc-cli stop
rm -f minderd
rm -rf bin
rm -rf node_data_dir
```

### Official Link <a href="#official-link" id="official-link"></a>

* [Twitter](https://twitter.com/mvcglobal)&#x20;
* [Discord](https://discord.com/invite/RGHWazu9eS)&#x20;
* [Explorer](https://scan.mvc.space/)
* &#x20;[Website](https://www.mvc.space/miners)\
