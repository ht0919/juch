# Chromebook(ARM版)のLinux環境にJupyter Notebookを導入する

## 概要

ARM系のChromebook(Lenovo S330)で、Linux環境にJupyter Notebookを導入しました。その作業手順を解説します。

## ハードウェア

今回使用するChromebookは次の機種です。

    機種名：Lenovo Chromebook S330
    モニタ：14.0型フルHD液晶(TN)
    CPU：MediaTek MT8173C
    メモリ：4GB
    ストレージ：64GB(eMMC)

## Linux環境の導入

Linux環境は次の作業でインストールします。

    1. 画面右下で時間表示をクリックする
    2. [設定]をクリックする
    3. [Linux（beta）]をクリックし、[有効にする]をクリックする
    4. 画面の指示に従って設定を進める
    5. 最後にターミナルウィンドウが開くので、Linuxコマンドを入力して動作確認する

## Linuxのバージョン

執筆時点(2020/08/23)での「cat /etc/os-release」の実行結果は次の通りです。

    NAME="Debian GNU/Linux"
    VERSION_ID="10"
    VERSION="10 (buster)"
    VERSION_CODENAME=buster
    ID=debian
    HOME_URL="https://www.debian.org/"
    SUPPORT_URL="https://www.debian.org/support"
    BUG_REPORT_URL="https://bugs.debian.org/"REPORT_URL="https://bugs.debian.org/"

## パッケージの更新(update.sh)

    $ sudo apt-get update
    $ sudo apt-get upgrade -y
    $ sudo apt-get dist-upgrade
    $ sudo apt-get autoclean

## PIP3の導入

    $ sudo apt install -y python3-pip python3-dev

## 数学関連パッケージの導入
    
    $ sudo apt install -y python3-numpy python3-scipy python3-matplotlib
    
## 機械学習関連パッケージの導入

    $ sudo apt install -y python3-pandas python3-sklearn
    
## Jupyter Notebookの導入

    $ sudo apt install -y jupyter-notebook

## Jupyter Notebookの起動

    $ jupyter notebook

## 仮想環境関連パッケージの導入

    $ sudo apt install -y python3-venv

## その他のパッケージ

- 必要に応じて「sudo apt install python3-モジュール名」、または「sudo pip3 install モジュール名」で追加してください。