# MkDocs ドキュメントサイト

認証・認可に関する技術ドキュメントをMkDocsで提供するプロジェクトです。

## セットアップ（Dev Container）

### 必要な環境

- Docker Desktop
- Visual Studio Code
- Dev Containers 拡張機能

### 起動手順

1. リポジトリをクローン

   ```bash
   git clone git@github.com:ry-miyamoto-sts/mkdocs.git
   cd mkdocs
   ```

2. VS Code で開く

   ```bash
   code .
   ```

3. コマンドパレット（`Ctrl+Shift+P` または `Cmd+Shift+P`）を開き、
   `Dev Containers: Reopen in Container` を選択

4. コンテナ起動後、ターミナルで以下を実行

   ```bash
   cd docs
   mkdocs serve -a 0.0.0.0:8000
   ```

5. ブラウザで `http://localhost:8000/` にアクセス

## ローカル環境での起動（Dev Container不使用）

```bash
cd docs
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

ブラウザで `http://127.0.0.1:8000/` にアクセスしてください。

## GitHub Pagesへのデプロイ

このプロジェクトはGitHub Actionsを使って自動的にGitHub Pagesにデプロイされます。

### 公開URL

- **ドキュメントサイト**: <https://ry-miyamoto-sts.github.io/mkdocs/>

### デプロイ方法

1. `main` ブランチにプッシュすると自動的にデプロイされます
2. 手動でデプロイする場合:
   - GitHubリポジトリの「Actions」タブを開く
   - 「Deploy MkDocs to GitHub Pages」ワークフローを選択
   - 「Run workflow」ボタンをクリック

### 初回セットアップ（リポジトリ管理者のみ）

1. GitHubリポジトリの「Settings」→「Pages」を開く
2. 「Source」で「Deploy from a branch」を選択
3. 「Branch」で `gh-pages` ブランチと `/ (root)` を選択
4. 「Save」をクリック

※ 初回のGitHub Actionsワークフロー実行後、`gh-pages` ブランチが自動作成されます。

## プロジェクト構成

```text
docs/
├── mkdocs.yml          # MkDocs設定ファイル
├── requirements.txt    # Python依存パッケージ
└── src/               # ドキュメントソース
    ├── index.md
    ├── auth-basics.md
    ├── oauth-oidc-basics.md
    └── ...
```
