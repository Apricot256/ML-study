# ML-study

## overview
サークルの機械学習の勉強会用の資料やコードを置いておくリポジトリ

## スケジュール
- day01 パーセプトロン
    - 機械学習の概要
    - 教師あり学習
    - 特徴量スケーリング
    - 確率的勾配降下法
- day02 分類問題(i)
    - パーセプトロンの決定
    - ロジスティック回帰
    - 線形SVM
    - 非線形SVM
- day03 分類問題(ii)
    - 決定木
    - ランダムフォレスト
    - k最近傍法

## 環境
環境構築には Docker と Visual Studio Code の Dev Containers 拡張機能を利用します。  
事前に以下のものをインストールしておいてください。
- Docker Engine 
[Windows](https://docs.docker.com/desktop/install/windows-install/) /
[Mac](https://docs.docker.com/desktop/install/mac-install/) /
[Linux](https://docs.docker.com/desktop/install/linux-install/)
- Visual Studio Code [install](https://code.visualstudio.com/download)
- Dev Containers Extention Code [install](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## 説明資料のコンパイル
`.devcontainer/Dockerfile` の12行目をコメントアウトすると環境構築時に
LaTexで書かれている資料をコンパイルするための環境がインストールされる。(時間がかかるのでデフォルトでコメントアウトしてあります)  
LaTexの環境を有効化したら以下の手順でPDFファイルにコンパイルすることができる。

説明資料が置いてあるディレクトリに移動
```
cd Presentation
```

すべての資料をコンパイル
```
make
```

生成物(PDF含む)を削除
```
make clean
```