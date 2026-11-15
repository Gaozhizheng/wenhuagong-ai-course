# 文化宫 AI 课程 · 配套项目库

徐州市文化宫《从想法到作品：AI 创作实战课》的配套公开仓库，存放课堂使用的 Skills、示例项目与课程资料。

## 分区

| 目录 | 内容 | 状态 |
|---|---|---|
| `skills/` | 课堂 Skill 的展开文件夹，可直接安装 | 已建 |
| `dist/` | Skill 的离线 ZIP 分享包 | 已建 |
| `projects/` | 课堂示例项目 | 规划中，用到再开 |
| `courseware/` | 课件与参考资料 | 规划中，用到再开 |

## 当前收录

| Skill | 中文名 | 版本 | 说明 |
|---|---|---|---|
| `jimeng-image-workshop` | 即梦图像工坊 | v2.0 | 把一句话需求变成能直接粘贴到即梦的中文生图提示词；覆盖文生图、改图、融图、组图、优化已有提示词。只给词与操作指引，不生成图片、不调 API |

## 别人怎么安装

仓库里的 skill 是**展开的文件夹**（内含 `SKILL.md`），不是需要先解压的压缩包。GitHub 链接本身不会自动安装，需要下面这一步：

```bash
git clone https://github.com/Gaozhizheng/wenhuagong-ai-course.git
```

然后把整个 skill 文件夹放进客户端扫描的技能目录：

- 用户级（所有项目可用）：`~/.workbuddy/skills/`
- 项目级（仅当前项目）：`<项目根>/.workbuddy/skills/`

Windows 命令提示符：

```bat
xcopy /E /I "wenhuagong-ai-course\skills\jimeng-image-workshop" "%USERPROFILE%\.workbuddy\skills\jimeng-image-workshop"
```

macOS / Linux：

```bash
cp -r wenhuagong-ai-course/skills/jimeng-image-workshop ~/.workbuddy/skills/
```

**新建会话或重启客户端**（技能列表在启动时扫描），说一句「用即梦图像工坊帮我做张图」验证是否触发。部分客户端支持从 GitHub 仓库安装技能并自动做安全审计，也可以用那种方式。

适用边界：读 `SKILL.md` 的技能机制（WorkBuddy / CodeBuddy / Claude 系）。豆包、Coze 等不认 `SKILL.md` 的平台不能直接当技能装，ZIP 只作传输载体，内容需另行适配。

## 离线分发

`dist/jimeng-image-workshop.zip` 是标准分享包，包内根目录为 skill 文件夹名、`SKILL.md` 在这一层；解压后按同样方式安装。ZIP 与 `skills/` 下的展开版本保持同版本。

## 版本记录

| 日期 | 内容 |
|---|---|
| 2026-11-15 | 仓库建立；加入 `jimeng-image-workshop` v2.0（4 个 Markdown + 离线 ZIP） |
