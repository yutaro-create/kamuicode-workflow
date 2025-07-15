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

## 🔍 ステップ6: トラブルシューティング

### 6.1 一般的な問題

#### API Key関連
- Claude API Keyの確認
- 使用量制限の確認

#### MCP設定関連
- kamuicode MCP設定の確認
- 必要なツールの有効化確認

#### 権限関連
- PAT_TOKENの権限確認
- リポジトリアクセス権限の確認

### 6.2 デバッグ方法

1. **Actions実行ログを確認**
   - 各ステップの詳細ログを確認
   - エラーメッセージを特定

2. **ファイル生成状況を確認**
   - 中間ファイルの生成状況
   - ファイルサイズと形式

3. **API制限の確認**
   - レート制限の確認
   - 使用量の確認

## 🎯 ステップ7: カスタマイズ

### 7.1 音楽設定の調整
- 音楽の長さ: 30-40秒
- 音楽の品質: 高品質
- 音楽ジャンル: 自由指定

### 7.2 画像設定の調整
- 画像サイズ: 1024x1024
- 画像数: 3枚
- 画像スタイル: 音楽に合わせて自動

### 7.3 動画設定の調整
- 動画の長さ: 5秒/セグメント
- 動画品質: 1080p
- フレームレート: 24fps

## 📊 ステップ8: 監視とメンテナンス

### 8.1 実行状況の監視
- Actions実行履歴の確認
- 成功率の監視
- エラーパターンの分析

### 8.2 定期メンテナンス
- [ ] API使用量の確認
- [ ] ストレージ使用量の確認
- [ ] ワークフロー実行回数の確認
- [ ] 生成物の品質確認

## 🎵 ステップ9: 使用例

### 9.1 基本的な使用方法

```bash
# 音楽コンセプトの例
"サイバーパンク都市の夜景、エレクトロニック、ネオンライト"
"未来の東京、シンセウェイブ、80年代レトロ"
"ロボットダンス、テクノ音楽、メカニカル"
```

### 9.2 高度な使用方法

```bash
# 詳細な指定
"120BPMのテクノ音楽、暗い雰囲気、工場の映像、産業的、モノクロ"
"穏やかなアンビエント、森の中、自然の音、鳥のさえずり、緑豊か"
```

## 🚀 完了

セットアップが完了しました！

**次のステップ:**
1. テスト実行で動作確認
2. 本格的な音楽動画生成
3. 結果の確認と調整
4. 継続的な改善

---

**サポート:**
- Issue報告: GitHub Issues
- ドキュメント: README.md
- 使用例: EXAMPLES.md