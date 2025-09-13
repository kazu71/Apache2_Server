# Ubuntu Server で簡単な Apache2　サーバを立ててみる
この記事では、Apache2 webサーバをUbuntu Server OSで立ち上げる手順をシンプルに説明している記事です。

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

> [３，Apache2 インストール[]()](https://github.com/kazu71/Apache2_Server/blob/main/README.md#apache2%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E5%8F%8A%E3%81%B3%E8%B5%B7%E5%8B%95%E3%81%AF%E4%BB%A5%E4%B8%8B%E3%81%AE%E8%A8%98%E8%BC%89%E9%80%9A%E3%82%8A%E3%81%AE%E9%A0%86%E7%95%AA%E3%81%A7%E8%A1%8C%E3%81%84%E3%81%BE%E3%81%99)
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
