# Open SSH Serverのインストール
https://codechacha.com/ja/ubuntu-install-openssh/  
を参考にした。
```bash
$ sudo apt update
$ sudo apt install openssh-server

$ sudo systemctl status ssh
```
もし実行されていない場合は、次のコマンドで実行する。
```bash
$ sudo systemctl enable ssh
$ sudo systemctl start ssh
```
