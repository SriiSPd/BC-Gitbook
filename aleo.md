---
description: Guide Aleo Testnet
---

# Aleo

\
​[​<img src=".gitbook/assets/twitter-removebg-preview.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg) [Twitter BeritaCryptoo](https://twitter.com/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png) [Telegram BeritaCryptoo](https://t.me/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png) [Discord BeritaCryptoo](https://discord.gg/beritacryptoonode)​

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FoCuKsbtqiSgg53794xg5%2F185994172-0b4e4ea8-f81a-48db-8020-9be619f485b7.png?alt=media&#x26;token=5b5c3f32-f276-48ab-95b4-c397e8116eba" alt=""><figcaption></figcaption></figure>

#### Auto Setup <a href="#auto-setup" id="auto-setup"></a>

```
wget -O aleo.sh https://raw.githubusercontent.com/Megumiiiiii/Aleo/main/aleo.sh && chmod +x aleo.sh && ./aleo.sh
```

Jika muncul pilihan (y/N) ketik y lalu enterJika muncul pilihan seperti ini, ketik 1 lalu enter​

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FjnJySkXwENZR5cDwtaYo%2FScreenshot_52.png?alt=media&#x26;token=29091a80-f298-4a3b-bf84-e9261100f59a" alt=""><figcaption></figcaption></figure>

Yak, disini lama

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FqJaclnc7nVaCiqtZbXLC%2FScreenshot_62.png?alt=media&#x26;token=b82245a0-b9a5-470c-8b4a-1623928de49f" alt=""><figcaption></figcaption></figure>

<img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2Fc93QCYwgS8dVr0jP4W1z%2Fncvbn.png?alt=media&#x26;token=a752f8c1-6785-49fb-81c1-1cf32281999f" alt="" data-size="line">Jangan lupa **BACKUP** **SEMUA** data(PrivKey dan teman2nya) yang muncul setelah install

#### Setelah selesai download dan install, jalankan <a href="#setelah-selesai-download-dan-install-jalankan" id="setelah-selesai-download-dan-install-jalankan"></a>

```
cd snarkOS
screen -S aleo
./run-prover.sh
```

Masukan Private Key yang tadi

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FOlQzWK56PKahu50VMerI%2FScreenshot_63.png?alt=media&#x26;token=dd4bf099-6b3b-4cce-ab4f-0fad99224f2f" alt=""><figcaption></figcaption></figure>

> * `CTRL+A+D` untuk close
> * Untuk kembali, pakai command `screen -Rd aleo`

#### OK! <a href="#ok" id="ok"></a>

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FTh3Zk6PitscuGTh90gnU%2FScreenshot_64.png?alt=media&#x26;token=fb379816-75ad-42ec-a5a6-8cc899019085" alt=""><figcaption></figcaption></figure>

#### Jika ingin uninstall Node <a href="#jika-ingin-uninstall-node" id="jika-ingin-uninstall-node"></a>

```
cd ~/snarkOS
rustup self uninstall
```

```
cd
rm -f aleo.sh
rm -rf snarkOS
```
