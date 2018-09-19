# README #

- Pull したあとは, 35行目の IPアドレスを適当な値に変更する

~~~
config.vm.network "private_network", ip: "192.168.33.10"
~~~

# How to start vagrant

~~~
$ vagrant status
$ vagrant up
$ vagrant status
~~~

# How to use vagrant

~~~
$ vagrant ssh
$ vagrant halt
~~~

以上の作業で virtual box 上に仮想マシンが作成される．

# その後の作業

~~~
vagrant ssh

# OSを最新状態にアップデート（時間かかります）
sudo yum -y update

# スクリプトを入手するためのgitをインストール
sudo yum -y install git

# Git の設定
git config --global user.name "Koichiro Rinsaka"
git config --global user.email "a@a.b.com"
git config --global color.ui true
git config -l

# Github に設置された centos6ansible のクローンを作成（コピー）し，実行すれば，各種開発環境がインストール・設定される．
git clone git@github.com:rinsaka/centos6vagrantfile.git

# エラーが出た場合は Github のWebサイト https://github.com/rinsaka/centos6ansible からzip形式でダウンロードして展開する．
unzip centos6ansible.git
~~~

- その後のインストール作業は centos6ansible/README.MD を参照してください．
