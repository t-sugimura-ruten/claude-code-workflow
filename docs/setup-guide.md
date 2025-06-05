# セットアップガイド

## 前提条件

1. GitHubアカウント
2. リポジトリへのWrite権限
3. Anthropic APIキー

## セットアップ手順

### 1. APIキーの設定

1. リポジトリの `Settings` → `Secrets and variables` → `Actions`
2. `New repository secret` で以下を追加：
   - **Name**: `ANTHROPIC_API_KEY`
   - **Secret**: あなたのAnthropic APIキー

### 2. GitHub Actionsの有効化

1. リポジトリの `Actions` タブでワークフローを確認
2. 必要に応じてワークフローを有効化

### 3. 基本的な使い方

イシューコメントで `@claude-code` をメンションしてタスクを指定：

```
@claude-code Hello Worldを出力するPythonファイルを作成してください
```

## トラブルシューティング

### ワークフローが実行されない
1. Actions タブでワークフロー実行ログを確認
2. APIキーが正しく設定されているか確認
3. タスクの内容が明確か確認

### 実行エラーが発生する
1. Actions タブで実行ログをアーティファクト保存
2. ログの内容を確認
3. イシューでエラー内容を報告
