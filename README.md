# Claude Code GitHub Workflow

Claude CodeをGitHub Actionsで自動実行するワークフローです。

## 🚀 概要

このリポジトリは、GitHub IssuesでClaude Codeをメンションすることで、自動的にコード生成・修正を行うシステムのデモンストレーションです。

## ✨ 特徴

- **自動化されたコード生成**: イシューコメントでタスクを指定するだけ
- **GitHub Actions連携**: シームレスな実行環境
- **実行履歴の保存**: `.claude-code/`ディレクトリに自動保存
- **多言語対応**: JavaScript、Python等の言語に対応

## 🏗️ プロジェクト構成

```
claude-code-workflow/
├── .claude-code/          # Claude Code実行履歴（自動生成）
├── .github/workflows/     # GitHub Actions設定
├── docs/                  # ドキュメント
│   ├── setup-guide.md    # セットアップガイド
│   └── usage-examples.md # 使用例
├── examples/              # サンプルコード
│   ├── hello.js
│   ├── hello.py
│   └── main.py
├── README.md              # このファイル
├── CLAUDE.md              # Claude Code向け指示
└── .gitignore
```

## 🔧 セットアップ

### 前提条件

- GitHubアカウント
- リポジトリへの管理者権限
- Anthropic APIキー

### インストール手順

1. **リポジトリのフォーク**
   ```bash
   # このリポジトリをフォークしてください
   ```

2. **APIキーの設定**
   - リポジトリの `Settings` → `Secrets and variables` → `Actions`
   - `New repository secret` で `ANTHROPIC_API_KEY` を追加

3. **GitHub Actionsの有効化**
   - `Actions` タブでワークフローを確認・有効化

詳細な手順は [セットアップガイド](docs/setup-guide.md) をご覧ください。

## 📝 使用方法

### 基本的な使い方

1. **イシューを作成**
2. **コメントでタスクを指定**:
   ```
   @claude-code Hello Worldを出力するPythonファイルを作成してください
   ```
3. **自動実行を待つ**
4. **結果を確認**

### 使用例

```
@claude-code package.jsonファイルを作成してください
```

```
@claude-code app.jsファイルのバグを修正してください
```

```
@claude-code utilsモジュールのテストを追加してください
```

詳細な使用例は [使用例ドキュメント](docs/usage-examples.md) をご覧ください。

## 🔍 ワークフローの仕組み

1. **トリガー**: イシューコメントで `@claude-code` をメンション
2. **実行**: GitHub ActionsがClaude Codeを起動
3. **処理**: タスクの解析・コード生成・ファイル操作
4. **結果**: コミット・プッシュ・コメント返信

## 📊 実行履歴

すべての実行履歴は `.claude-code/` ディレクトリに自動保存されます:

- `issues/issue-{番号}/`: 各イシューの実行履歴
- `summary.md`: 実行概要
- `latest-output.txt`: 最新の出力結果

## 🛠️ トラブルシューティング

### よくある問題

**ワークフローが実行されない**
- APIキーが正しく設定されているか確認
- GitHub Actionsが有効になっているか確認

**実行エラーが発生する**
- Actions タブで詳細ログを確認
- タスク内容が明確か確認

**タスクが理解されない**
- より具体的で明確な指示に変更
- 技術要件を明示

## 🤝 貢献

1. このリポジトリをフォーク
2. フィーチャーブランチを作成 (`git checkout -b feature/amazing-feature`)
3. 変更をコミット (`git commit -m 'Add amazing feature'`)
4. ブランチにプッシュ (`git push origin feature/amazing-feature`)
5. プルリクエストを作成

## 📄 ライセンス

このプロジェクトはMITライセンスの下で公開されています。

## 🔗 関連リンク

- [Claude Code公式ドキュメント](https://docs.anthropic.com/)
- [GitHub Actions](https://github.com/features/actions)
- [Anthropic API](https://www.anthropic.com/api)

---

**🎯 今すぐ試す**: イシューを作成して `@claude-code Hello World` とコメントしてみてください！
