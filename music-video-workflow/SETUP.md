# セットアップガイド

AI Music Video Generator Workflowのセットアップ手順

## 📋 前提条件

- GitHub リポジトリ（Actions有効）
- Claude API アクセス
- kamuicode MCP サーバー設定

## 🔧 ステップ1: リポジトリ設定

### 1.1 ワークフローファイルの配置

```bash
# ワークフローファイルを配置
mkdir -p .github/workflows
cp create-music-video.yml .github/workflows/
```

### 1.2 kamuicode MCP設定

```bash
# MCP設定ディレクトリを作成
mkdir -p .claude

# kamuicode MCP設定ファイルを配置
# .claude/mcp-kamuicode.json の設定が必要
```

## 🔐 ステップ2: Secrets設定

### 2.1 必要なSecrets

以下のキーの設定が必要です：

```
ANTHROPIC_API_KEY  # Claude API Key
PAT_TOKEN          # GitHub Personal Access Token (repo権限)
```

### 2.2 Secrets設定手順

1. **リポジトリのSettings** → **Secrets and variables** → **Actions**
2. **New repository secret**をクリック
3. 上記のSecretsを追加

## 📁 ステップ3: ディレクトリ構造

```
your-repo/
├── .github/
│   └── workflows/
│       └── create-music-video.yml
├── .claude/
│   └── mcp-kamuicode.json
├── README.md
└── (他のファイル)
```

## 🎛️ ステップ4: 権限設定

### 4.1 Actions権限

**Settings** → **Actions** → **General**

- ✅ Allow all actions and reusable workflows
- ✅ Allow GitHub Actions to create and approve pull requests

### 4.2 Workflow権限

**Settings** → **Actions** → **General** → **Workflow permissions**

- ✅ Read and write permissions
- ✅ Allow GitHub Actions to create and approve pull requests

## 🧪 ステップ5: テスト実行

### 5.1 手動テスト

1. **Actions**タブに移動
2. **Create AI Music Video**ワークフローを選択
3. **Run workflow**をクリック
4. 音楽コンセプトを入力（例: "サイバーパンク都市のテクノ音楽"）
5. **Run workflow**を実行

### 5.2 動作確認

実行後、以下を確認：

- [ ] 音楽ファイルが生成されている
- [ ] 3つの画像が生成されている
- [ ] 3つの動画が生成されている
- [ ] 最終ミュージックビデオが生成されている
- [ ] Pull Requestが自動作成されている

---

**サポート:**
- Issue報告: GitHub Issues
- ドキュメント: README.md
- 使用例: EXAMPLES.md