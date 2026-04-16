---
{"dg-publish":true,"permalink":"//claude-code-cli/","dgPassFrontmatter":true,"dg-note-properties":{}}
---

# [Claude Code 配置](https://longcat.chat/platform/docs/zh/ClaudeCode.html#claude-code-%E9%85%8D%E7%BD%AE)

## [概述](https://longcat.chat/platform/docs/zh/ClaudeCode.html#%E6%A6%82%E8%BF%B0)

本指南将详细介绍如何配置Claude Code CLI工具，使其使用LongCat API开放平台的服务。LongCat API开放平台完全兼容 Anthropic Claude API 格式，您只需简单配置，即可在Anthropic API生态中使用LongCat模型能力。

## [前置条件](https://longcat.chat/platform/docs/zh/ClaudeCode.html#%E5%89%8D%E7%BD%AE%E6%9D%A1%E4%BB%B6)

**1. 获取 API Key**

在开始配置之前，您需要：

1. 访问 [LongCat API开放平台](https://longcat.chat/platform/)
2. 注册并完成账户创建
3. 登录后前往 [API Keys](https://longcat.chat/platform/api_keys) 页面
4. 获取您的 API Key（需要用户自行手动创建）

**2. 确认 Claude Code 已安装**

确保您已经安装了 Claude Code CLI 工具。如果尚未安装，请参考[官方文档](https://docs.anthropic.com/zh-CN/docs/claude-code/setup)进行安装。

## [配置方法](https://longcat.chat/platform/docs/zh/ClaudeCode.html#%E9%85%8D%E7%BD%AE%E6%96%B9%E6%B3%95)[Claude code新手小白保姆级入门教程｜从零开始学习 Claude code](../Clippings/Claude%20code新手小白保姆级入门教程｜从零开始学习%20Claude%20code.md)

Claude Code 支持通过配置文件进行精细的控制。

**1. 创建配置文件**

创建或编辑 Claude Code 配置文件：`~/.claude/settings.json`

```
{
  "env": {
    "ANTHROPIC_AUTH_TOKEN": "your_longcat_api_key",
    "ANTHROPIC_BASE_URL": "https://api.longcat.chat/anthropic",
    "ANTHROPIC_MODEL": "LongCat-Flash-Chat",
    "ANTHROPIC_SMALL_FAST_MODEL": "LongCat-Flash-Chat",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "LongCat-Flash-Chat",
    "ANTHROPIC_DEFAULT_OPUS_MODEL": "LongCat-Flash-Chat",
    "CLAUDE_CODE_MAX_OUTPUT_TOKENS": "6000",
    "CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC": 1
  },
  "permissions": {
    "allow": [],
    "deny": []
  }
}
```

**2. 支持的模型**

LongCat API开放平台目前提供以下模型：

|模型名称|API格式|描述|
|---|---|---|
|LongCat-Flash-Chat|OpenAI/Anthropic|高性能通用对话模型|
|LongCat-Flash-Thinking|OpenAI/Anthropic|深度思考模型|
|LongCat-Flash-Thinking-2601|OpenAI/Anthropic|升级版深度思考模型|
|LongCat-Flash-Lite|OpenAI/Anthropic|高效轻量化MoE模型|

## [测试 Claude Code](https://longcat.chat/platform/docs/zh/ClaudeCode.html#%E6%B5%8B%E8%AF%95-claude-code)

启动 Claude Code 并发送一个简单的测试消息：

```
claude
```

然后输入测试消息，如："你好，请介绍一下自己"

如果配置正确，您将收到来自LongCat模型的回复。


{

"env": {

"ANTHROPIC_AUTH_TOKEN": "ak_2a918t8ij54i86c1t19He1XP9bD1i",

"ANTHROPIC_BASE_URL": "https://api.longcat.chat/anthropic",

"ANTHROPIC_MODEL": "LongCat-Flash-Thinking-2601",

"ANTHROPIC_SMALL_FAST_MODEL": "LongCat-Flash-Thinking-2601",

"ANTHROPIC_DEFAULT_SONNET_MODEL": "LongCat-Flash-Thinking-2601",

"ANTHROPIC_DEFAULT_OPUS_MODEL": "LongCat-Flash-Thinking-2601",

"CLAUDE_CODE_MAX_OUTPUT_TOKENS": "6000",

"CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC": 1

},

"permissions": {

"allow": [],

"deny": []

}

}