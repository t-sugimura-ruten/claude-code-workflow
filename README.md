# Claude Code GitHub Workflow

Claude CodeをGitHub Actionsで自動実行するワークフローです。

## 🚀 概要

このプロジェクトは、GitHub Issues経由でClaude Codeを実行し、結果をコミットとして自動保存するワークフローを提供します。

## 📋 セットアップ

### 1. API キーの設定

1. リポジトリの `Settings` → `Secrets and variables` → `Actions`
2. `New repository secret` で以下を追加：
   - **Name**: `ANTHROPIC_API_KEY`
   - **Secret**: あなたのAnthropic APIキー

### 2. ワークフローの有効化

GitHub Actionsが有効になっていることを確認してください。

## 🎯 使用方法

### Issue経由でのタスク実行

GitHub Issuesで `@claude-code` をメンションしてタスクを指定：

```
@claude-code Hello Worldを出力するPythonファイルを作成してください
```

## 📁 プロジェクト構成

```
claude-code-workflow/
├── .claude-code/              # Claude Code実行履歴（自動生成）
├── .github/
│   └── workflows/
│       └── claude-code-official.yml  # GitHub Actions ワークフロー
├── docs/                      # ドキュメント
├── examples/                  # サンプルファイル
│   ├── hello.js              # JavaScript Hello World
│   ├── hello.py              # Python Hello World
│   └── main.py               # メイン実行ファイル
├── README.md                  # このファイル（人間向け）
├── CLAUDE.md                  # Claude Code向け指示
└── .gitignore
```

## 🔧 開発ステータス

- ✅ 基本ワークフロー（Stage 1）
- ⏳ 高度なワークフロー（Stage 2 - 予定）
- ⏳ イシューテンプレート（Stage 3 - 予定）

## 🐛 トラブルシューティング

### ワークフローが実行されない
1. `ANTHROPIC_API_KEY` が設定されているか確認
2. イシューコメントで `@claude-code` と正確にメンションしているか確認
3. GitHub Actionsが有効になっているか確認

### 実行エラーが発生する
1. Actions タブでワークフロー実行ログを確認
2. APIキーが正しく設定されているか確認
3. タスクの内容が明確か確認

## 📚 関連リンク

- [Claude Code 公式ドキュメント](https://docs.anthropic.com/)
- [GitHub Actions ワークフロー構文](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions)

## 🤝 コントリビューション

このプロジェクトへの貢献を歓迎します。以下の方法で参加できます：

- バグ報告
- 機能提案
- プルリクエスト
- ドキュメント改善

---

**テスト方法**: このリポジトリでIssueを作成し、コメントで `@claude-code Hello World` とメンションしてみてください！
