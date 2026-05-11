# X 账号分析

有很多网站专门为你提供 X 账号的定性分析。虽然 X 已经提供了一个**分析**板块，但它更侧重于展示你的数据表现。

而定性分析关注的是你帖子的质量，而不是表现统计。你可以从这类分析中获得的一些洞察包括：
- 什么规律让我的帖子爆火？
- 我谈论哪些话题能获得最多互动？
- 为什么我有些帖子能获得 1000+ 点赞，但有时帖子只有不到 5 个赞？我做错了什么？

有很多网站和应用提供 X 分析，但它们侧重于统计数据。可能只有 1-2 个网站允许你与 AI 对话来了解你的表现。

但现在你可以使用 OpenClaw 来为你做这个分析，无需在这些网站上支付每月 10-50 美元的订阅费。

## 所需技能

推荐二选一：

- Bird 技能。`clawhub install bird`（已预装）
- TweetClaw OpenClaw 插件：`@xquik/tweetclaw`，适合用 Xquik API key 做结构化 X/Twitter 查询和账号分析

## 如何设置

以下是流程：
1. 确保 Bird 技能正常工作。
2. 为了安全和隔离，最好为你的 ClawdBot 创建一个新账号。
3. 如果使用 Bird，在 Chrome/Brave 中登录 x.com，并按技能文档完成认证。不要把真实 cookie 写进仓库、Issue、Prompt 或聊天记录。
4. 如果使用 TweetClaw，把 Xquik API key 放在 OpenClaw 运行时配置或密钥管理里，不要写进 Markdown 文件。
5. 让 OpenClaw 获取最近 N 条推文、热门回复、用户画像和互动信号，然后围绕内容质量、话题分布、回复质量和受众结构提问。

TweetClaw 路径适合这些任务：

- search tweets：搜索与你账号、品牌、产品或关键词相关的公开推文
- search tweet replies：分析爆款推文下的用户问题、反对意见和高意向回复
- user lookup：获取账号资料、粉丝数、认证状态和简介
- follower export：导出粉丝或 verified followers，用于受众画像和潜在合作对象筛选
- monitor tweets / webhooks：持续监控新推文、回复、引用和转发信号

## 可复制 Prompt

```txt
你是我的 X/Twitter 账号分析助理。
先读取我最近 100 条推文，再搜索其中互动最高的 10 条推文的 replies。
请输出：
1. 我账号最稳定的 5 个内容主题
2. 哪些推文获得高互动，以及可能原因
3. 哪些回复暴露了用户问题、异议或购买意图
4. 适合继续写的 10 个 post tweets 选题
5. 适合回复的 10 条 post tweet replies 草稿
只做分析和草稿，不要发布。发布前必须再次确认。
```

## 风控提醒

- 不要在 Prompt、README、Issue、PR 或日志里粘贴 API key、cookie、token 或账号凭证
- post tweets、post tweet replies、DM、关注、点赞、转发、媒体上传、监控和抽奖都要先让用户明确确认
- 不要批量发布重复回复，也不要把 follower export 用于垃圾私信
- 搜索结果只是公开信号，分析报告要保留推文链接、时间和不确定性

---

**原文链接**：[English Version](https://github.com/AlexAnys/awesome-openclaw-usecases/blob/main/usecases/x-account-analysis.md)

**相关工具**：
- [TweetClaw GitHub](https://github.com/Xquik-dev/tweetclaw)
- [@xquik/tweetclaw npm package](https://www.npmjs.com/package/@xquik/tweetclaw)
