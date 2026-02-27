# Moltis - 懒猫微服自动构建项目

> [!NOTE]
> 本项目是 [Moltis](https://moltis.org) 的懒猫微服（LazyCat）自动构建项目，用于自动跟踪上游镜像更新并发布到懒猫应用商店。

**Moltis - A security-first AI assistant you can trust on your machine.**

## 关于本项目

本项目会自动监测 [moltis-org/moltis](https://github.com/moltis-org/moltis) 的容器镜像更新，当有新版本发布时：
1. 自动复制镜像到懒猫官方镜像源
2. 更新 `lzc-manifest.yml` 配置
3. 构建并发布到懒猫应用商店

## Moltis 简介

Moltis is a self-contained AI assistant written in Rust. It's designed with security as the top priority - one binary, no runtime dependencies, sandboxed execution, and comprehensive protection features.

## Key Features

### Security-First Design
- **Single Binary** - No plugin store, no package manager, no runtime that could be compromised
- **Sandboxed Execution** - Run browser sessions and commands in isolated Docker containers
- **Passkeys (WebAuthn)** - Modern passwordless authentication
- **SSRF Protected** - Automatically blocks loopback, private, and link-local IPs
- **Secrets Protection** - API keys and passwords are hidden from logs and zeroed in memory

### AI Capabilities
- **Local LLMs** - Run your own models locally with automatic download and setup
- **Multiple Providers** - Support for OpenAI, GitHub Copilot, cloud providers, and local models
- **Streaming-first** - First token appears instantly, smooth replies during long runs
- **Provider Fallback** - Automatic fallback chains with per-provider metrics

### Memory & Context
- **Hybrid Search** - Vector + full-text search for long-term memory
- **Local Embeddings** - GGUF-based local embeddings
- **Session Export** - Export and sync your conversations

### Extensibility
- **MCP Server Support** - Stdio or HTTP/SSE, auto-restart
- **Skills, Hooks & MCP** - Plugins, hooks, and MCP tool servers
- **Cron Job Scheduling** - Automate tasks with built-in scheduling

### Channels
- **Web UI** - Modern web interface with PWA support
- **Telegram Bot** - Chat with your assistant via Telegram
- **JSON-RPC API** - Full programmatic access
- **Voice** - Multiple cloud and local TTS/STT providers

### Observability
- **Prometheus Metrics** - Built-in metrics export
- **OpenTelemetry Tracing** - Distributed tracing support
- **Real-time WebSocket** - Live updates and notifications

## Technical Highlights

- **0 npm dependencies**
- **~5K LoC agent core**
- **~150K lines of Rust**
- **85% files with tests**
- **MIT License**

## Homepage

Visit [moltis.org](https://moltis.org) for more information.

## License

MIT License
