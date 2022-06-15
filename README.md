# cloud_build_sample

本リポジトリは Cloud Build と連携するリポジトリです

## 環境詳細

- Python : 3.9

### 事前準備

- Docker インストール
- VS Code インストール
- VS Code の拡張機能「Remote - Containers」インストール
  - https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers
- 本リポジトリの clone
- `.env` ファイルを空ファイルでプロジェクト直下に作成
- 以下をプロジェクト名に合わせて変更
  - `.devcontainer/devcontainer.json`
    - `name`, `service`
  - `docker-compose.yml`
    - `services` の Key 名
    - `image`, `container_name`
    - `env_file`
      - 環境変数を使用しない場合は除去
  - main.py
  - logging.conf
    - `hoge` を使用するモジュール名に合わせる
  - `README.md`
  - `LICENSE`
  - dependabot
    - `.github/dependabot.yml`
    - `.github/workflows/auto_merge_depandabot.yml`
  - pyproject.toml
    - `tool.poetry.name`, `tool.poetry.description`, `tool.poetry.authors`

### 開発手順

1. VS Code 起動
2. 左下の緑色のアイコンクリック
3. 「Remote-Containersa: Reopen in Container」クリック
4. しばらく待つ
   - 初回の場合コンテナー image の取得や作成が行われる
5. 起動したら開発可能
