# kamuicode Workflows

AI content generation workflow templates using Claude Code SDK and kamuicode MCP

## Overview

This repository provides workflow templates for generating AI content using Claude Code SDK and kamuicode MCP in GitHub Actions.

## Included Workflows

### 🎵 Music Video Generation Workflow
AI-powered automatic music video generation workflow

- **Google Lyria** music generation (30-40 seconds, high quality)
- **Imagen4 Fast** image generation (3 images)
- **Hailuo-02 Pro** video generation (3x 5-second videos)
- **FFmpeg** video editing and integration
- Automatic pull request creation

Details: [music-video-workflow/](./music-video-workflow/)

### 📹 Video Generation Workflow
AI-powered automatic video generation workflow

- **Imagen4 Ultra** high-quality image generation
- **Vidu Q1** reference video generation
- Automatic pull request creation

Details: [video-workflow-template/](./video-workflow-template/)

## Requirements

- Claude Code SDK
- kamuicode MCP
- Anthropic API Key
- GitHub Actions

## Quick Start

1. Select the workflow template you want to use
2. Copy the template files to your repository
3. Add required Secrets and MCP configuration
4. Run the workflow

## License

MIT License

## Contributing

We welcome PRs for new workflow templates and bug fixes.

---

🤖 Powered by [Claude Code SDK](https://github.com/anthropics/claude-code) & [kamuicode MCP](https://www.kamui.ai/ja)