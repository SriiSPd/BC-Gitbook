# Prepare Setelah Mendapat Personal Token

​[​<img src="https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg) [Twitter BeritaCryptoo](https://twitter.com/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png) [Telegram BeritaCryptoo](https://t.me/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png) [Discord BeritaCryptoo](https://discord.gg/beritacryptoonode)

### Install Keperluan

```
sudo apt update; sudo apt upgrade
sudo apt install curl wget gnupg apt-transport-https -y
```

```
curl -fsSL https://packages.erlang-solutions.com/ubuntu/erlang_solutions.asc | sudo gpg --dearmor -o /usr/share/keyrings/erlang.gpg
```

```
echo "deb [signed-by=/usr/share/keyrings/erlang.gpg] https://packages.erlang-solutions.com/ubuntu $(lsb_release -cs) contrib" | sudo tee /etc/apt/sources.list.d/erlang.list
```

```
sudo apt update

sudo apt install erlang-base erlang-public-key erlang-ssl
```

### Download Tea Client

```
wget https://tea.thepower.io/teaclient

chmod +x teaclient
```

### Membuat Folder Baru

```
mkdir {db,log}
mkdir /root/log/deinfra; mkdir /root/db/deinfra
```

### Download Docker Images

```
docker pull thepowerio/tpnode
```

{% hint style="info" %}
<mark style="color:blue;">**Note**</mark>: Baru bisa mulai setelah mendapat Chain Token dari mereka
{% endhint %}
