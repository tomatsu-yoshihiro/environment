# Goのインストール

## 最新版のGoをダウンロードする
```bash
wget https://dl.google.com/go/goX.YY.Z.linux-amd64.tar.gz
```

## ダウンロードしたパッケージを解凍する
```bash
sudo tar -C /opt -xzf goX.YY.Z.linux-amd64.tar.gz
```

## Go用に環境変数を設定する
Ubuntuの場合はホームディレクトリにある`.profile`の末尾に以下を追記します。
```bash
export PATH=$PATH:/opt/go/bin
export GOPATH=~/go
export GOROOT=/opt/go
```

## 環境構築例
https://dev.classmethod.jp/articles/go-setup-and-sample/

## Goのモジュール管理
https://zenn.dev/spiegel/articles/20210223-go-module-aware-mode
