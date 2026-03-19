# OpenClaw Template

OpenClaw 安装模板项目，让你快速克隆并开始使用 OpenClaw。

## 快速开始

### 1. 克隆项目

```bash
git clone https://github.com/The27149/openclaw-template.git
cd openclaw-template
```

### 2. 安装依赖

```bash
npm install
```

### 3. 配置环境变量

运行 setup 脚本：

```bash
npm run setup
```

这会：
- 创建 `.env` 文件（从 `.env.example` 复制）
- 引导你编辑配置
- 可选运行 `openclaw onboard`

### 4. 编辑 .env 文件

打开 `.env` 文件，填入你的 API Keys：

```env
# 必需：至少配置一个 AI 模型提供商
OPENAI_API_KEY=sk-...
# 或
ANTHROPIC_API_KEY=sk-ant-...

# 可选：配置消息通道
TELEGRAM_BOT_TOKEN=123456:ABCDEF...
DISCORD_BOT_TOKEN=MTIzNDU2...
```

### 5. 初始化 OpenClaw

```bash
npx openclaw onboard --install-daemon
```

### 6. 启动 Gateway

```bash
npx openclaw gateway
```

## 环境变量说明

查看 `.env.example` 文件了解所有可配置的环境变量：

- **AI 模型 API Keys**: OpenAI, Anthropic, OpenRouter 等
- **消息通道**: Telegram, Slack, Discord 等
- **路径配置**: 自定义 OpenClaw 主目录
- **日志配置**: 调整日志级别

## 常用命令

```bash
# 启动 gateway
npx openclaw gateway

# 打开控制面板
npx openclaw dashboard

# 发送测试消息
npx openclaw message send --target +1234567890 --message "Hello"

# 检查状态
npx openclaw gateway status
```

## 文档

- [OpenClaw 官方文档](https://docs.openclaw.ai)
- [Getting Started](https://docs.openclaw.ai/start/getting-started)
- [配置参考](https://docs.openclaw.ai/gateway/configuration)

## 许可证

ISC  
