# セットアップガイド

## ディレクトリ構造

```
your-repo/
├── .github/
│   ├── workflows/
│   │   ├── create-video-from-prompt.yml    # 手動実行ワークフロー
│   │   └── issue-video-trigger.yml         # Issue連動ワークフロー
│   └── ISSUE_TEMPLATE/
│       └── video-request.md                 # Issueテンプレート
└── .claude/
    └── mcp-kamuicode.json                   # MCP設定（別途準備必要）
```

## 手順

### 1. ファイルのコピー

```bash
# ワークフローファイル
cp create-video-from-prompt.yml .github/workflows/
cp issue-video-trigger.yml .github/workflows/

# Issueテンプレート（オプション）
cp .github/ISSUE_TEMPLATE/video-request.md .github/ISSUE_TEMPLATE/
```

### 2. GitHub Secretsの設定

リポジトリの Settings → Secrets and variables → Actions で以下を設定：

- **ANTHROPIC_API_KEY** (必須)
  - Claude APIキー
  - [Anthropic Console](https://console.anthropic.com/)で取得

- **PAT_TOKEN** (オプション)
  - GitHub Personal Access Token
  - より高度な権限が必要な場合に使用

### 3. MCP設定の準備

`.claude/mcp-kamuicode.json` ファイルを作成し、kamuicodeのMCP設定を記述。

### 4. 権限の確認

リポジトリの Settings → Actions → General で以下を確認：

- **Workflow permissions**: "Read and write permissions" を選択
  - 理由: ワークフローが新しいブランチを作成し、ファイルをコミット・プッシュするため
  
- **Allow GitHub Actions to create and approve pull requests**: チェック
  - 理由: 最終ステップで生成した動画をプルリクエストとして自動作成するため

これらの権限がないと、ワークフローは以下のエラーで失敗します：
- ブランチ作成時: `Permission denied to create branch`
- PR作成時: `Resource not accessible by integration`

## 使い方

### Issueテンプレートを使用

1. Issues → New Issue
2. 「AI動画生成リクエスト (I2V)」を選択
3. コンセプトを記入して送信

### 手動実行

1. Actions → Create Video from Prompt
2. Run workflow → プロンプト入力 → Run

### コメントでトリガー

```markdown
@create-video-i2v
コンセプト：夕焼けの海岸線を歩く人影
```

## トラブルシューティング

### ワークフローが起動しない
- Secretsが正しく設定されているか確認
- ワークフローファイルがデフォルトブランチにあるか確認

### 動画生成が失敗する
- APIキーの有効性を確認
- MCP設定ファイルの内容を確認
- Actions のログを確認

### Issueからトリガーできない
- `issue-video-trigger.yml` が存在するか確認
- リポジトリの権限設定を確認