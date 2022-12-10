# Menghubungkan Repo di Github dengan Gitopia

## Official Docs

{% embed url="https://docs.gitopia.com/mirror" %}

<mark style="color:red;"><mark style="color:orange;"><mark style="color:green;">**Pastikan sudah memiliki akun GitHub**<mark style="color:green;"><mark style="color:orange;"></mark>

### 1. Fork Repository

* [https://github.com/Megumiiiiii?tab=repositories](https://github.com/Megumiiiiii?tab=repositories)
* [https://github.com/xsons?tab=repositories](https://github.com/xsons?tab=repositories)
* Atau buat repo sendiri, **BEBAS**

### 2. Create a Repository di Gitopia

Nama Bebas

<figure><img src="../.gitbook/assets/Connect Github.png" alt=""><figcaption></figcaption></figure>

### 3. Masuk ke repository Github mu yang ingin dihubungkan

### 4. Klik Setting

<figure><img src="../.gitbook/assets/masuk ke setting.png" alt=""><figcaption></figcaption></figure>

### 5. Scroll dan Masuk ke Secret -> Action

<figure><img src="../.gitbook/assets/secret action.png" alt=""><figcaption></figcaption></figure>

### 6. Pilih New Secret

<figure><img src="../.gitbook/assets/new secret.png" alt=""><figcaption></figcaption></figure>

### 7. Beri nama dan masukan isi

* Nama:

```
GITOPIA_WALLET
```

* Isi menggunakan data dari wallet yang di download dari tutor sebelumnya. [Tutor Sebelumnya](https://beritacryptoo.gitbook.io/node/gitopia/membuat-repo-dari-0)

<figure><img src="../.gitbook/assets/isi secret.png" alt=""><figcaption></figcaption></figure>

Gitu

<figure><img src="../.gitbook/assets/Gitu.png" alt=""><figcaption></figcaption></figure>

### 8. Lanjut ke Action

<figure><img src="../.gitbook/assets/Pilih Action.png" alt=""><figcaption></figcaption></figure>

### 9. Pilih Simple workflow

<figure><img src="../.gitbook/assets/pilih simple.png" alt=""><figcaption></figcaption></figure>

**a. Ganti nama file .yml**

Dari `blank.yml`

<figure><img src="../.gitbook/assets/ganti menjadi.png" alt=""><figcaption></figcaption></figure>

Menjadi `gitopia-mirror.yml`

<figure><img src="../.gitbook/assets/gini.png" alt=""><figcaption></figcaption></figure>

**b. Hapus isinya**

**c. Ganti dengan ini**

```
name: Mirror to Gitopia

on:
  push:
    branches:
      - '**'

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
        with:
          fetch-depth: 0
      - name: Push to Gitopia mirror
        uses: gitopia/gitopia-mirror-action@v0.5.0
        with:
          gitopiaWallet: "${{ secrets.GITOPIA_WALLET }}"
          remoteUrl: "link-repo-gitopia-mu"
          force: false

```

`link-repo-gitopia-mu` ganti dengan link dari sini

<figure><img src="../.gitbook/assets/url ini.png" alt=""><figcaption></figcaption></figure>

Isi file `.yml` sekarang

<figure><img src="../.gitbook/assets/Isi yaml.png" alt=""><figcaption></figcaption></figure>

**d. Klik Start Commit**

<figure><img src="../.gitbook/assets/start commit.png" alt=""><figcaption></figcaption></figure>

### **10. Kembali ke web gitopia**

### **11. Refresh dan Cek hasilnya**

<figure><img src="../.gitbook/assets/Selesai.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Selesaiiii.png" alt=""><figcaption></figcaption></figure>



### **Fork Repository di Gitopia**

* [https://gitopia.com/BeritaCryptooDAO/Testnet-Tutorial](https://gitopia.com/BeritaCryptooDAO/Testnet-Tutorial)
* [https://gitopia.com/megumii/Guide-Testnet](https://gitopia.com/megumii/Guide-Testnet)
* [https://gitopia.com/megumii/Connect-Github](https://gitopia.com/megumii/Connect-Github)
