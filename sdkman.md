# SDKMANのUbuntuへのインストール
https://zenn.dev/y_u_t_a/articles/e7dd725c868b7b

## ZIPのインストール
ZIPがインストールされていない場合は以下を実行する。
```bash
sudo apt install zip
```

## SDKMANのインストール
```bash
curl -s "https://get.sdkman.io" | bash
```

## SDKMANの有効化
```bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
```

## Javaのインストール
```bash
# インストール可能な Java 一覧
sdk list java
# AdoptOpenJDK 15 をインストールする
sdk i java 15.0.2.j9-adpt
# Java のインストール確認
java -version
# 再ログインしたら JAVA_HOME が設定される
exec $SHELL -l
echo $JAVA_HOME
```