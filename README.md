# kamuicode Workflows

Claude Code SDK と kamuicode MCP を活用したAI生成ワークフロー集

## 概要

このリポジトリは、GitHub ActionsでClaude Code SDKとkamuicode MCPを使用してAIコンテンツを生成するワークフローテンプレートを提供します。

## 含まれるワークフロー

### 🎵 Music Video Generation Workflow
AIを使用した自動音楽動画生成ワークフロー

- **Google Lyria** による音楽生成（30-40秒、高品質）
- **Imagen4 Fast** による画像生成（3枚）
- **Hailuo-02 Pro** による動画生成（3つの5秒動画）
- **FFmpeg** による動画編集・統合
- 自動プルリクエスト作成

詳細: [music-video-workflow/](./music-video-workflow/)

### 📹 Video Generation Workflow
AIを使用した自動動画生成ワークフロー

- **Imagen4 Ultra** による高品質画像生成
- **Vidu Q1** による参照動画生成
- 手動実行とIssue経由の両方に対応
- 自動プルリクエスト作成

詳細: [video-workflow-template/](./video-workflow-template/)

### 🎬 Video with Background Removal Workflow
背景除去機能を含む動画生成ワークフロー

- 背景除去処理
- 動画生成
- 自動プルリクエスト作成

詳細: [video-background-removal-workflow/](./video-background-removal-workflow/)

### 🔍 Gemini I2V Analysis Workflow
Gemini APIを使用した画像から動画生成の分析ワークフロー

- 画像分析
- 動画生成最適化
- 品質評価

詳細: [gemini-i2v-workflow/](./gemini-i2v-workflow/)

## 必要な環境

- Claude Code SDK
- kamuicode MCP
- Anthropic API Key
- GitHub Actions

## クイックスタート

1. 使用したいワークフローテンプレートを選択
2. テンプレート内のファイルを自分のリポジトリにコピー
3. 必要なSecretsとMCP設定を追加
4. ワークフローを実行

## ライセンス

MIT License

## 貢献

新しいワークフローテンプレートの追加やバグ修正のPRを歓迎します。

---

🤖 Powered by [Claude Code SDK](https://github.com/anthropics/claude-code) & [kamuicode MCP](https://www.kamui.ai/ja)