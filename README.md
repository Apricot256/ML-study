# ML-study

## overview
サークルの機械学習の勉強会用の資料やコードを置いておくリポジトリ

## スケジュール
<details>
<summary>Day01 基礎</summary>

- 機械学習とは
- 教師あり学習にチャレンジ
- 特徴量スケーリング
- 確率的勾配降下法
</details>

<details>
<summary>Day02 分類問題(i) </summary>

- パーセプトロンの欠点
- ロジスティック回帰
- 線形SVM
- 非線形SVM
</details>

<details>
<summary>Day03 分類問題(ii)</summary>

- 決定木
- ランダムフォレスト
- k最近傍法
</details>

<details>
<summary>Day04 データの前処理</summary>

- 欠損値の処理
- カテゴリデータの整形
- 正則化
</details>

<details>
<summary>Day05 次元削減</summary>

- 主成分分析
- 線形判別分析
- カーネル主成分分析
</details>

## 環境
環境構築には Docker と Visual Studio Code の Dev Containers 拡張機能を利用します。  
事前に以下のものをインストールしておいてください。
- Docker Engine 
[Windows](https://docs.docker.com/desktop/install/windows-install/) /
[Mac](https://docs.docker.com/desktop/install/mac-install/) /
[Linux](https://docs.docker.com/desktop/install/linux-install/)
- Visual Studio Code [install](https://code.visualstudio.com/download)
- Dev Containers Extention [install](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

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