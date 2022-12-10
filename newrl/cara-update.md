# Cara Update

### 1.

```
screen -X -S xxxx.newrl quit
```

`xxxx` di sesuaikan dengan angka dari `screen -ls`

### 2.

```
cd ~/newrl-venv/newrl
scripts/install.sh mainnet
```

#### 3.

```
screen -S newrl
```

```
scripts/start.sh mainnet --fullnode
```
