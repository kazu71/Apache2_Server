# Ubuntu Server で簡単な Apache2　サーバを立ててみる
この記事では、Apache2 webサーバをUbuntu Server OSで立ち上げる手順をシンプルに説明している記事です。より細かな説明は今後記載予定ですのでしばらくお待ちください。

> [１，Ubuntu Serverを更新する](https://github.com/kazu71/Ubuntu_System_Administration/blob/4b5e9cec90f7cb2ace2f518c08a5ca8412f95cf3/update_system/README.md)
#### 更新は以下の記載通りの順番で行います。

```
sudo apt update
```
```
sudo apt upgrade
```
``` 
sudo reboot
```
> [２、ufw インストール](https://github.com/kazu71/Ubuntu_System_Administration/tree/4b5e9cec90f7cb2ace2f518c08a5ca8412f95cf3/UFW_System)
#### ポート開放の設定管理システムのインストール及び起動を以下の記載通りの順番で行います。

```
sudo apt install ufw
```
```
sudo systemctl enable ufw
```
```
sudo systemctl start ufw
```
```
sudo ufw allow 80
```

> [３，Apache2 インストール]()
#### apache2のインストール及び起動は以下の記載通りの順番で行います。
```
sudo apt install apache2
```
```
sudo systemctl enable apache2 
```
```
sudo systemctl start apache2
```
```
sudo systemctl status apache2
```
#### この時点で、apache2 webサーバにアクセスが可能になります。
サイトを立ち上げているサーバからアクセスする場合
http://localhost:80

サーバと同じローカル上のPCからアクセスする場合
http://｛サーバIP｝:80
