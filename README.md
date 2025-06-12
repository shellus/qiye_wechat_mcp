# 企业微信消息 MCP 服务器

超简单的企业微信群机器人 MCP 服务器，让 AI 助手能发送消息到企业微信群。

## 快速开始

### 1. 安装依赖
```bash
pip install mcp requests python-dotenv
```

### 2. 配置企业微信群机器人
1. 在企业微信群中添加群机器人
2. 复制机器人的 Webhook URL

### 3. 设置环境变量
```bash
cp .env.example .env
# 编辑 .env 文件，填入你的 Webhook URL
```

### 4. 运行服务器
```bash
python server.py
```

### 5. 配置 Claude Desktop
在 Claude Desktop 配置文件中添加：
```json
{
  "mcpServers": {
    "企业微信": {
      "command": "python",
      "args": ["server.py"],
      "cwd": "/path/to/this/directory",
      "env": {
        "WECHAT_WEBHOOK_URL": "你的webhook地址"
      }
    }
  }
}
```

## 功能
- `send_text_message(content)` - 发送文本消息
- `send_markdown_message(content)` - 发送Markdown消息

就这么简单！
