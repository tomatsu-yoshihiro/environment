# Pythonインストール
## 必要なツールのダウンロード
```bash
$ sudo apt update
$ sudo apt install build-essential libbz2-dev libdb-dev \
  libreadline-dev libffi-dev libgdbm-dev liblzma-dev \
  libncursesw5-dev libsqlite3-dev libssl-dev \
  zlib1g-dev uuid-dev tk-dev
```
## Pythonソースのダウンロード
```bash
$ wget https://www.python.org/ftp/python/x.y.z/Python-x.y.z.tar.xz
$ tar xJf Python-x.y.z.tar.xz
```

## ビルド
```bash
$ cd Python-x.y.z
$ ./configure --enable-optimizations
$ make
$ sudo make install
```
