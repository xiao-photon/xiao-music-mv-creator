# 晓·音乐 MV 创作

给 Codex 一套制作音乐 MV 和预告片的工作流程。你可以从歌曲想法开始，也可以把已有音轨、歌词、参考图或分镜交给它，从当前阶段接着做。

## 安装

1. 克隆或下载此仓库，保留整个 `xiao-music-mv-creator` 文件夹。
2. 将文件夹复制到当前项目的 `.agents/skills/` 下。从其他项目也要调用时，可复制到你的主目录下的 `.agents/skills/`。
3. 在目标项目中打开 Codex，用 `$xiao-music-mv-creator` 调用。列表里还没出现时，重启 Codex 再试。 [Codex Skill 加载说明](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

装好后的项目结构如下。

```text
你的项目/
└── .agents/
    └── skills/
        └── xiao-music-mv-creator/
            ├── SKILL.md
            ├── agents/
            │   └── openai.yaml
            └── references/
```

## 快速试用

```text
用 $xiao-music-mv-creator 为《雨停以后》设计一条 12 秒的竖屏 MV 预告。
音轨还没生成。气质是雨夜转晴后的松弛，人物穿墨绿防雨外套，场景是夜间公交站。
请交一份适合出歌的风格提示词、一份覆盖 12 秒的预告剪辑草案，并给核心镜头写独立的静帧词和图生视频词。这次只要文字。
```

你应该拿到一份出歌提示词、一张覆盖目标时长的剪辑表，以及两条完整的镜头提示词。音乐切点会先标为暂定，图生视频词会写清待用的首帧。

## 包里有什么

| 文件 | 用途 |
|---|---|
| [Skill 主入口](xiao-music-mv-creator/SKILL.md) | 判断当前制作阶段，按需读取对应流程。 |
| [核心提示词库](xiao-music-mv-creator/references/prompt-library.md) | 9 组可复制模板和 3 条完整文本示例。 |
| [音乐制作](xiao-music-mv-creator/references/music-track.md) | 歌词、风格提示、试听选版、定稿音轨与分镜的交接。 |
| [分镜执行与状态](xiao-music-mv-creator/references/execution-pack.md) | 分镜表、独立静帧词与视频词、局部返工。 [项目状态与回退](xiao-music-mv-creator/references/project-state.md) |
| [预告片](xiao-music-mv-creator/references/mv-teaser.md) | 选音乐、查素材、编排镜头、写剪辑时间线。 |
| [封面与发布素材](xiao-music-mv-creator/references/cover-release.md) | 原图和色彩约束、标题和封面交付。 |

只做创意、提示词和剪辑表时，用 Codex 即可。实际出歌、生图、生视频和导出成片需要相应工具以及可用的素材，由你的工作环境提供。
