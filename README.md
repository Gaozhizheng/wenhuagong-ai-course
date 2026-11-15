<div align="center">

# 文化宫 AI 课程 · 配套技能库

**把课堂里调教好的 AI 技能，装进任何人的桌面端 AI 客户端**

![skills](https://img.shields.io/badge/skills-1-185FA5) ![version](https://img.shields.io/badge/skill-v2.0-534AB7) ![format](https://img.shields.io/badge/Agent%20Skills-SKILL.md-0F6E56)

</div>

> 徐州市文化宫《从想法到作品：AI 创作实战课》配套仓库。这里放的不是讲义，而是**能直接装进 AI 里、立刻改变它干活方式**的技能包。

---

## 收录的技能

| 技能 | 做什么 | 版本 | 入口 |
|---|---|---|---|
| **即梦图像工坊** `jimeng-image-workshop` | 把一句模糊的生图需求，变成能直接粘到即梦的中文提示词；也支持改图、融图、组图、优化已有提示词 | v2.0 | [skills/jimeng-image-workshop](skills/jimeng-image-workshop) |

你只说「想做张卖茶叶的图」，它会问清用途和风格，给一段可直接复制的提示词和一句操作指引。**不生成图片、不调 API、不需要密钥**；图片在即梦里由你自己生成。

---

## 一键安装

### 方式一 · 把这段话发给你的 AI（推荐，真正的一键）

复制下面整段，粘贴到你的桌面端 AI 客户端对话框里发送即可。它会自动下载、放到正确目录、告诉你结果：

```
请帮我安装一个技能。
仓库：https://github.com/Gaozhizheng/wenhuagong-ai-course
步骤：
1. 把仓库下载到本地（clone 或下载 ZIP 均可）
2. 找到 skills/jimeng-image-workshop/ 这个文件夹，它里面直接有 SKILL.md
3. 把整个文件夹复制到你的用户级 skills 目录（WorkBuddy / CodeBuddy 用 ~/.workbuddy/skills/，Claude Code 用 ~/.claude/skills/，其他客户端用你自己的技能目录）
4. 不要多套一层目录，装完列出技能名，并告诉我要不要重启
```

适用于 WorkBuddy、CodeBuddy、Claude Code、Cursor、Codex 等**任何能读写本地文件的桌面端 agent**。这也是目前各家技能市场通用的安装形态：复制一段安装指令发给自己的 AI，由它完成下载与配置。

### 方式二 · 客户端自带的安装入口

| 客户端 | 做法 |
|---|---|
| WorkBuddy / CodeBuddy | 技能面板 →「导入 / 上传技能」选择技能包；或在技能管理里用「从 URL 安装」粘贴仓库链接。部分版本支持 `/install-skill <仓库链接>` 一类命令，**以你当前版本的入口为准** |
| Claude 桌面版 | 设置 → Customize → Skills → 上传 `dist/jimeng-image-workshop.zip` |
| Claude Code | `npx skills add Gaozhizheng/wenhuagong-ai-course --skill jimeng-image-workshop`，或手动把文件夹放进 `~/.claude/skills/` |
| 其他兼容 Agent Skills 的客户端 | 用方式一，让客户端自己定位技能目录 |

### 方式三 · 手动一行命令

Windows 命令提示符：

```bat
git clone https://github.com/Gaozhizheng/wenhuagong-ai-course.git
xcopy /E /I "wenhuagong-ai-course\skills\jimeng-image-workshop" "%USERPROFILE%\.workbuddy\skills\jimeng-image-workshop"
```

macOS / Linux：

```bash
git clone https://github.com/Gaozhizheng/wenhuagong-ai-course.git
cp -r wenhuagong-ai-course/skills/jimeng-image-workshop ~/.workbuddy/skills/
```

Claude Code 把目标目录换成 `~/.claude/skills/` 即可。

### 方式四 · 离线 ZIP

下载 [dist/jimeng-image-workshop.zip](dist/jimeng-image-workshop.zip)，解压得到 `jimeng-image-workshop/` 文件夹，放进技能目录。

> **装完请新建会话或重启客户端**：技能列表只在启动时扫描。

---

## 各客户端能不能装

| 客户端 | 支持 | 说明 |
|---|---|---|
| WorkBuddy / CodeBuddy | ✅ | 标准 `SKILL.md` 机制，用户级 `~/.workbuddy/skills/` |
| Claude Code / Claude 桌面版 | ✅ | 文件夹或 ZIP 上传 |
| Cursor、Codex 等兼容 Agent Skills 的客户端 | ✅ | 用方式一，让客户端自己定位技能目录 |
| 豆包、Coze 等网页版助手 | ❌ | 不读取本地 `SKILL.md`，也没有本地技能目录；ZIP 只能当资料传递，内容需另行适配 |

---

## 装好之后怎么用

直接在对话里说需求就会自动触发，例如：

- 「用即梦图像工坊，帮我做一张茶叶电商主图」
- 传一张图说「你看看能怎么改」
- 贴一段写好的提示词说「帮我优化一下」

也可以直接问它「怎么用」，会得到一段极简说明。

---

## 常见问题

**装完没反应？** 重启客户端或新建会话；确认 `SKILL.md` 直接在技能文件夹里，别多套一层目录。

**会不会自动出图、扣费？** 不会。技能只产出提示词和一句操作指引，不生成图片、不调 API、不需要密钥。

**安全吗？** 本仓库技能是纯 Markdown 指令，无脚本、无联网请求、不读凭据。安装任何第三方技能前，仍建议先看一眼 `SKILL.md`。

---

## 目录结构

```text
wenhuagong-ai-course/
├── skills/jimeng-image-workshop/    展开的技能文件夹（推荐安装方式）
├── dist/jimeng-image-workshop.zip   离线分享包
└── skills/README.md                 技能清单与维护约定
```

后续会按课程进度加入更多技能、示例项目与课件资料。

---

徐州市文化宫《从想法到作品：AI 创作实战课》 · 公开仓库，欢迎 clone 与转发
