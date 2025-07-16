# 開発環境構築手順（Docker + Rails）

このプロジェクトでは、Docker を利用して Rails アプリケーションの開発環境を構築します。以下の手順に従ってセットアップを進めてください。

---

以下のように整理すると、箇条書きとしての体裁を保ちつつ、読者が何をすべきかがより明確になります：

---

## 前提
* OSにはLinux(WSLでも可)を使用してください
    * ディストリビューションはUbuntu(Debian系であればOK)

## 1. 事前準備：必要なアプリケーションの確認

以下のアプリケーションがインストールされていることを確認してください。各ツールが正しく動作するかは、バージョン確認コマンドで確認できます。

* **Docker**

  ```bash
  docker --version
  ```

  ※コマンドを実行してバージョンが表示されない場合は、[こちら](https://www.docker.com/)からインストールしてください。

* **Docker Compose**

  ```bash
  docker-compose --version
  ```
  ※コマンドを実行してバージョンが表示されない場合は、[こちら](https://docs.docker.com/compose/install/)からインストールしてください。

* **Git**

  ```bash
  git --version
  ```
  ※コマンドを実行してバージョンが表示されない場合は、[こちら](https://git-scm.com/book/ja/v2/%E4%BD%BF%E3%81%84%E5%A7%8B%E3%82%81%E3%82%8B-Git%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)からインストールしてください。

---

## 2. 環境構築実施

### ① リポジトリのクローン

```bash
git clone https://github.com/arunbababa/rails-docker.git
cd rails-docker
```

### ② Docker コンテナの起動

以下のコマンドを実行して、Docker コンテナを起動します。

```bash
docker-compose up
```

※初回起動時は、イメージのビルドや依存関係のインストールに数分かかる場合があります。

### ③ 動作確認

ブラウザで以下のURLにアクセスしてください：

```
http://localhost:3000
```

以下のような表示がされていれば、セットアップは完了です。

![alt text](image.png)

---