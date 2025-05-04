# 🎉 Welcome to 42 Environments 🎉

このプロジェクトは、[42Tokyo](https://42tokyo.jp/)の課題開発に最適な環境を、**Docker**を用いて簡単に再現することを目的としています。
Ubuntuベースの仮想環境には、**clang**や**valgrind**、**norminette**など、42プロジェクトに必要なツールがあらかじめインストールされています。

---

## 🚀 使用方法

1. **Docker Desktop** をインストール
   → [公式サイト](https://www.docker.com/) からインストールしてください。

2. **最新版の環境をダウンロード**
   → 以下のリリースページから `.zip` または `.tar.gz` をダウンロードして展開します：
   👉 [v1.0.0 リリースページ](https://github.com/urassh/ft_environments/releases/tag/v1.0.0)

   ```bash
   # 例（ターミナル操作の場合）
   wget https://github.com/urassh/ft_environments/archive/refs/tags/v1.0.0.zip
   unzip v1.0.0.zip
   cd ft_environments-1.0.0
   ```

3. **コンテナを起動**：

   ```bash
   docker compose up -d
   ```

4. **コンテナに入る**：

   ```bash
   docker compose exec 42env bash
   ```

   デフォルトの作業ディレクトリは `/urassh` です。ホスト側のプロジェクトと同期されているので、自由に編集可能です。

---

## 📦 主なインストール済みパッケージ

* **`build-essential`**
  C/C++開発に必要な基本的なビルドツール群（`gcc`, `g++`, `make` など）を含むパッケージ。
  👉 **C言語のコンパイルやMakefileの動作に必須。**

* **`clang`**
  LLVMベースの高性能なC/C++コンパイラで、GCCの代替として使用可能。
  👉 **42で推奨されているコンパイラ環境に近づけるために導入。**

* **`git`**
  分散型のバージョン管理システム。
  👉 **課題テンプレートのクローンや、コード管理に必要。**

* **`curl`**
  URLからデータを取得できるコマンドラインツール（HTTP, HTTPSなど）。
  👉 **スクリプトやライブラリのダウンロード、API通信に便利。**

* **`wget`**
  ファイルのダウンロードに使われるもう一つのツール。
  👉 **valgrindなどのソースコードを取得するために使用。**

* **`ca-certificates`**
  HTTPS接続のためのSSL証明書群。
  👉 **curlやgitでHTTPS通信を行う際に必要。**

* **`valgrind`**
  メモリリーク、未初期化変数、ヒープエラーなどを検出する静的解析ツール。
  👉 **C言語のメモリバグを検出するために使用。42の課題でよく使われる。**

* **`make`**
  Makefileに従ってコンパイルやビルドを自動化するツール。
  👉 **42の課題においてビルド自動化に不可欠。**

* **`python3.10`**
  Pythonの実行環境。
  👉 **`francinette`など一部のコードチェックツールの実行に必要。**

* **`python3-pip`**
  Pythonのパッケージ管理ツール。
  👉 **`norminette`や他のPythonツールをインストールするために使用。**

* **`python3.10-venv`**
  Pythonの仮想環境作成ツール。
  👉 **`francinette`やPythonベースのツールの依存関係を分離・管理するために使用。**

* **`python3.10-distutils`**
  Pythonモジュールのビルド・インストールに必要なライブラリ。
  👉 **一部のPythonツールで依存されているため導入。**

* **`libtool`, `automake`, `autoconf`**
  ソースコードからのビルド時に必要なツール群。
  👉 **valgrindなどをソースからビルドするために必要。**

* **`libc6-dbg`**
  GNU Cライブラリのデバッグ情報付きバージョン。
  👉 **gdbやvalgrindでの詳細なデバッグに使用される。(francinetteというテストツールを使うため入れました)**

* **`norminette`**（Python経由でインストール）
  42のCコードスタイルを自動チェックする公式ツール。
  👉 **コードのスタイルチェックに必須。**

---

## 🧑‍💻 貢献

バグ報告・改善提案・プルリクエスト大歓迎です！

---
