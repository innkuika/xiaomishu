**简体中文** | [English](README.en.md)

# 小秘书 · Xiaomishu

一个住在 Claude app 里的私人生活秘书，打包成一个 Claude 技能（skill）。装上之后，Claude 会先用几轮选择题认识你，再给你发布一个自己的待办库页面，设好每天早上过日程、晚上预告明天的提醒。之后它会主动关心你、帮你排日程、管待办和生活里那些老是忘的事。

A personal life-assistant for the Claude app, packaged as a Claude skill. It interviews you with a few rounds of multiple-choice questions, publishes your own to-do hub (an Artifact page with its own database), and sets up a daily morning walkthrough and evening preview. Instructions are in Chinese.

## 它由三部分组成

| 部分 | 放在哪 | 管什么 |
|---|---|---|
| 记忆 | Claude 的 memory | 你是谁、喜欢什么、不喜欢什么 |
| 待办库 | 一个 Artifact 页面 + 它自带的数据库 | 要做什么、什么时候做 |
| 节奏 | 定时任务（scheduled tasks） | 每天早晚主动来找你 |

待办库页面有这些标签：本周、项目、分类、收件箱、生活循环（理发、体检这类定期的事）、要买的、闲了玩、以后再说。

## 安装

需要 Claude app（网页、桌面或手机），并且账号能用技能（Skills）、Artifacts、记忆和定时任务。具体哪些功能可用取决于你的方案和设置。

1. 下载这个仓库：点右上角 **Code → Download ZIP**，解压。
2. 把里面的 `xiaomishu` 文件夹单独压缩成 `xiaomishu.zip`。
3. 在 Claude app 的设置里找到 **Skills**，上传 `xiaomishu.zip`。
4. 新开一个对话，说：**「帮我装小秘书」**。

接下来回答几轮选择题就行，大约 20–30 分钟。

## 为什么是技能，而不是一封“安装邮件”

技能是你自己亲手装上的，所以 Claude 会把它当成真正的指令。邮件、网页里的内容，Claude 只会当成资料，不会照着执行。这是故意的：要是一封邮件就能让 AI 自己装东西，那就是钓鱼的完美入口。

## 隐私

- 这个仓库里没有任何人的个人数据。你的待办库是你账号下的一个新页面，数据库是空的，默认只有你能看到。
- 小秘书不会替你发消息、付款、下单或预约，除非你每次都明确同意。详见 `xiaomishu/references/safety.md`。

## 文件

```
xiaomishu/
├── SKILL.md                    安装流程 + 日常规则
├── assets/hub-template.html    待办库页面
└── references/
    ├── onboarding.md           入门问卷
    ├── conventions.md          待办库数据规则
    ├── daily-rhythm.md         早晚提醒
    ├── persona.md              性格
    └── safety.md               不能做的事
```

## License

MIT
