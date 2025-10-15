# Dev Container 設定

このディレクトリには、VS Code Dev Container の設定が含まれています。

## 使い方

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

4. コンテナのビルドと起動が完了するまで待つ

5. ターミナルでMkDocsを起動
   ```bash
   cd docs
   mkdocs serve -a 0.0.0.0:8000
   ```

6. ブラウザで `http://localhost:8000` にアクセス

## 含まれる機能

- Python 3.12
- Git
- MkDocs と関連パッケージ（自動インストール）
- VS Code 拡張機能：
  - Python
  - Markdown All in One
  - markdownlint

## ポートフォワーディング

- ポート 8000 が自動的にフォワードされます
