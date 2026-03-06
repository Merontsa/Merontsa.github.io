# 作業記録

## 2026-03-06

### GitHub CLI (`gh`) のセットアップ

#### 背景
- ターミナルから GitHub を操作したいという要望
- `gh` コマンド（GitHub 公式 CLI ツール）を導入することにした

#### 実施内容

**1. インストール確認**
- 最初に `gh --version` を実行したところ `command not found` でインストールされていないことが判明

**2. インストール**
```bash
brew install gh
```
- Homebrew 経由で GitHub CLI v2.87.3 をインストール成功

**3. 認証**
```bash
gh auth login
```
- 認証方式: GitHub.com / ブラウザ認証
- ワンタイムコード `9424-04CA` を https://github.com/login/device に入力して認証
- GitHub アカウント `Merontsa` としてログイン完了

#### 結果
- `gh` コマンドが使用可能になった
- 以後、PR 作成・Issue 管理・リポジトリ操作などをターミナルから実施できる

#### 主要コマンドメモ
| コマンド | 説明 |
|---------|------|
| `gh repo list` | リポジトリ一覧を表示 |
| `gh repo view` | 現在のリポジトリ情報を表示 |
| `gh issue list` | Issue 一覧を表示 |
| `gh issue create` | Issue を作成 |
| `gh pr list` | Pull Request 一覧を表示 |
| `gh pr create` | Pull Request を作成 |
| `gh run list` | GitHub Actions の実行状況を確認 |
| `gh auth status` | 認証状態を確認 |
