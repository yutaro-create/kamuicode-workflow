# kamuicode Workflows

Claude Code SDK と kamuicode MCP を活用したAI生成ワークフロー集

## 概要

このリポジトリは、GitHub ActionsでClaude Code SDKとkamuicode MCPを使用してAIコンテンツを生成するワークフローテンプレートを提供します。

## 含まれるワークフロー

### 📹 Video Generation Workflow
AIを使用した自動動画生成ワークフロー

- **Imagen4 Ultra** による高品質画像生成
- **Vidu Q1** による参照動画生成
- 自動プルリクエスト作成

詳細: [video-workflow-template/](./video-workflow-template/)

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