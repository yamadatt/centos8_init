CentOS8.3の初期設定用のansible playbook

実施すること

## 事前設定

### ターゲットノード

初期設定対象のサーバは以下まで実施しておく。

* OSインストール
* IPアドレス付与
* SSHでのログイン

## ansibleノード

対象ホストの書き換え
localhostが対象サーバになっているので、これをターゲットサーバのIPアドレスに書き換える

## playbook概要

### packageの最新化

### SELinuxの無効化

### firewalldの無効化

### よく使うパッケージのインストール

* git
* samba

### 設定情報出力

SELinux,firewalldの状態。自分のホスト名。

### dockerのインストール

### docker-composeのインストール

### docker情報の出力

dockerのバージョン、

### GeForce GTX 1650 のドライバインストール

ドライバを入れると```nvidia-smi```が利用可能になる

### NVIDIA Container Toolkitのインストール

DockerからGPUを使うために必要



## 冪等性は保たれない

冪等性が保たれないので、使用するときは考慮が必要




## 環境

動作確認をした環境は以下。

* CentOS 8.3
* ansible 


```
$ ansible --version
ansible 2.10.9
  config file = None
  configured module search path = ['/root/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/lib/python3.6/site-packages/ansible
  executable location = /usr/local/bin/ansible
  python version = 3.6.8 (default, Aug 24 2020, 17:57:11) [GCC 8.3.1 20191121 (Red Hat 8.3.1-5)]
```

## 使い方

### 事前準備

事前に対象ホストにSSHして、鍵を登録しておく。

### コマンド


```
git clone https://github.com/yamadatt/centos8_init
cd centos8_init/
ansible-playbook -i hosts site.yml --ask-pass
```