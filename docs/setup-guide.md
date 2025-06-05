# セットアップガイド

## 前提条件

- GitHubアカウント
- Anthropic APIキー（[Anthropic Console](https://console.anthropic.com/)で取得）

## 1. リポジトリのフォーク・クローン

```bash
# このリポジトリをフォーク後、クローン
git clone https://github.com/YOUR_USERNAME/claude-code-workflow.git
cd claude-code-workflow
```

## 2. GitHub Secrets の設定

1. GitHubリポジトリページで `Settings` タブをクリック
2. 左サイドバーから `Secrets and variables` → `Actions` を選択
3. `New repository secret` をクリック
4. 以下の情報を入力：
   - **Name**: `ANTHROPIC_API_KEY`
   - **Secret**: あなたのAnthropic APIキー
5. `Add secret` をクリック

## 3. GitHub Actions の有効化

1. リポジトリの `Actions` タブをクリック
2. 「I understand my workflows, go ahead and enable them」をクリック
3. ワークフローが有効になることを確認

## 4. 動作確認

1. リポジトリで新しいIssueを作成
2. コメント欄に以下を入力：
   ```
   @claude-code Hello Worldを出力するシンプルなPythonファイルを作成してください
   ```
3. コメントを投稿
4. GitHub Actionsが自動実行されることを確認
5. 数分後にコミットが作成されることを確認

## トラブルシューティング

### ワークフローが実行されない場合

1. **APIキーの確認**
   - Secrets にAPIキーが正しく設定されているか確認
   - キーに余分なスペースや改行が含まれていないか確認

2. **GitHub Actions の権限確認**
   - Settings → Actions → General で権限設定を確認
   - "Allow all actions and reusable workflows" が選択されているか確認

3. **ワークフローファイルの確認**
   - `.github/workflows/claude-code-official.yml` が存在するか確認
   - ファイルの構文エラーがないか確認

### エラーログの確認方法

1. `Actions` タブを開く
2. 失敗したワークフロー実行をクリック
3. エラーメッセージを確認して問題を特定

## セキュリティ注意事項

- APIキーは絶対にコードにハードコードしない
- フォークしたリポジトリでのSecrets設定は各自で行う
- パブリックリポジトリでの機密情報の取り扱いに注意

## 次のステップ

セットアップが完了したら、[使用例ガイド](./usage-examples.md)を参照して、さまざまなタスクを試してみてください。
