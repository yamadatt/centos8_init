CentOS8.3の初期設定用のansible playbook

実施すること

## 事前設定

初期設定対象のサーバは以下まで実施しておく。

* OSインストール
* IPアドレス付与
* SSHでのログイン　鍵入れろと言われるから

## ansible側

対象ホストの書き換え
localhostが対象サーバになっているので、これをIPアドレスに書き換える

## playbookで実施すること

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






