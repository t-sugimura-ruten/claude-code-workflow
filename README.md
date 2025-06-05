# Claude Code GitHub Workflow

Claude CodeをGitHub Actionsで自動実行するワークフローです。

## 🚀 クイックスタート

### 1. APIキーの設定

1. リポジトリの `Settings` → `Secrets and variables` → `Actions`
2. `New repository secret` で以下を追加：
   - **Name**: `ANTHROPIC_API_KEY`
   - **Secret**: あなたのAnthropic APIキー

### 2. 基本的な使い方

イシューコメントで `@claude-code` をメンションしてタスクを指定：

```
@claude-code Hello Worldを出力するPythonファイルを作成してください
```

## 📋 現在の機能

### ✨ 基本ワークフロー
- イシューコメントでの `@claude-code` メンション検知
- Claude Codeの自動実行
- 実行結果のコメント投稿
- ログのアーティファクト保存

## 🎯 使用例

### シンプルなファイル作成
```
@claude-code package.jsonファイルを作成してください
```

### コード修正
```
@claude-code app.jsファイルのバグを修正してください
```

### テスト追加
```
@claude-code utilsモジュールのテストを追加してください
```

## 📁 ファイル構成

```
.github/
└── workflows/
    └── claude-code-basic.yml    # 基本ワークフロー
```

## 🔄 開発ステータス

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

## 📝 次のステップ

このワークフローが正常に動作することを確認したら、より高度な機能を追加予定：

- タスクタイプ別の自動分類
- プルリクエストの自動作成
- 複数ブランチ対応
- カスタムイシューテンプレート

---

**テスト方法**: このリポジトリでイシューを作成し、コメントで `@claude-code Hello World` とメンションしてみてください！
