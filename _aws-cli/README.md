# AWS ClI

## インストール

+ 公式ドキュメント
  + https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/install-cliv2-linux.html

### Linux x86

+ インストール

```
cd /usr/local/src
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

+ 確認

```
aws --version
```
```
$ aws --version
aws-cli/2.1.6 Python/3.7.3 Linux/5.4.0-1029-gcp exe/x86_64.ubuntu.20 prompt/off
```
