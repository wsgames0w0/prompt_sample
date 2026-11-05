# Prompt Sample

本リポジトリでは，Pythonのプロジェクトを対象としたコード支援系AIに渡すプロンプトの例を掲載する．

## 実行環境

- Python 3.10.11

## ディレクトリ構成

```
本リポジトリ
│
├─ common.md # コード支援系AIに渡す各プロジェクト共通のプロンプト
│
├─ prompt.md # コード支援系AIに渡す各プロジェクト固有のプロンプトのメモ
│
├─ LICENSE   # ライセンスファイル
│
├─ README.md # 本ファイル
│
```

## プロンプトの渡し方

0. [common.md](./common.md)の内容を一度はご確認ください

1. 下記のコマンドを実行し，Pythonの仮想環境(venv)を作成する

```
python -m venv venv
```

2. 下記のコマンド(Windows用)を実行し，仮想環境を起動する

```
.\venv\Scripts\activate
```

- pipの更新コマンド(最新バージョンをインストールできる時に実行)

```
python.exe -m pip install --upgrade pip
```

3. 下記のPythonライブラリをインストールする

```
tqdm
pandas
matplotlib
numpy
torch
torchvision
```

- インストールコマンド(torch，torchvisionを除く)

```
pip install tqdm pandas matplotlib numpy
```

- NVIDIA GPU CUDA11.8に対応したPytorchのインストール方法

```
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu118
```

4. 本リポジトリのcommon.mdとprompt.mdをコピーし，作業対象のプロジェクトディレクトリに配置する

5. 下記の編集前prompt.mdを，編集後prompt.mdのように編集する

- 編集前

~~~
# <ここにプロジェクト名を記述する>

## 最初のプロンプト

```
<ここにAIに渡すプロンプトを記述する>
```
~~~

- 編集後

~~~
# Prompt Sample

## 最初のプロンプト

```
`common.md`に従ってプログラムの実装やレポートの作成，GitHubへの掲載準備を行ってください．
本プロジェクトでは，本ディレクトリ内のファイルを確認し，GitHubに掲載するための`README.md`を作成してください．
```
~~~

6. prompt.mdに記載したプロンプトをコピーし，コード支援系AIに渡す

7. コード支援系AIがcommon.mdに従ってプログラムを作成し，プロンプトで渡されたタスクを行う

## ライセンス

本プロジェクトのソースコードおよびドキュメントは [MIT License](./LICENSE) のもとで公開されています．

## 最終更新

2026年11月05日．
