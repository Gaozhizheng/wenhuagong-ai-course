# 课堂 Skills

本目录存放展开形态的 skill，每个文件夹内含 `SKILL.md`，可直接放进客户端技能目录安装。安装步骤见仓库根 README。

| Skill | 中文名 | 版本 | 文件 | 说明 |
|---|---|---|---|---|
| `jimeng-image-workshop` | 即梦图像工坊 | v2.1 | 4 个 `.md` | 即梦（Seedream）生图提示词助手：从零生成、改图、融图、组图、参考图、优化已有提示词。只产出提示词与一句操作指引 |

离线 ZIP 在 `dist/`。

## 维护约定

- skill 实体升级后，同轮更新三处：本目录的展开文件夹、`dist/` 里的 ZIP、仓库根 README 的收录表版本号与徽章
- 目录名与 `SKILL.md` frontmatter 的 `name` 一致
- 分享包格式：`<skill-name>.zip`，包内根目录即 skill 文件夹名
