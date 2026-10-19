# AI 漫画工具选型手册

> ⭐ **Support This Project**
>
> [![GitHub stars](https://img.shields.io/github/stars/oeaf/ai-comic-tools?style=social)](https://github.com/oeaf/ai-comic-tools)
> [![GitHub forks](https://img.shields.io/github/forks/oeaf/ai-comic-tools?style=social)](https://github.com/oeaf/ai-comic-tools)
> [![GitHub issues](https://img.shields.io/github/issues/oeaf/ai-comic-tools)](https://github.com/oeaf/ai-comic-tools/issues)
>
> 如果这个项目对你有用，欢迎点个 ⭐ Star！你的支持是我持续更新的动力。

7 个 AI 漫画创作工具的归类选型手册。来源：[@CY160909（Shlcy）的推文推荐](https://x.com/CY160909/status/2111799455980658973)（2026-10-18），逐个核验仓库现状后整理。

它们覆盖漫画生产的不同环节：故事→分镜→画格→上色。一次收 7 个，逐条写进技能库又乱又重复，所以归到这一个仓库：**对比表 + 决策树 + 每家一页评估**。

## 对比总表（2026-10-19 评估）

| 工具 | 定位 | 工作流 | Star | 协议 |
|---|---|---|---|---|
| [AI Comic Factory](tools/ai-comic-factory.md) | 一句话出整页漫画 | 故事描述→LLM 分镜→SDXL 画图；官网直接玩 | 1349 | Apache-2.0（⚠️已归档只读） |
| [AI Comic Generator](tools/ai-comic-generator.md) | JSON 驱动完整工作流 | 故事→分镜 JSON→角色三视图→逐格生成→单格重画 | 15 | MIT（要 Gemini key） |
| [StoryDiffusion](tools/story-diffusion.md) | 人物一致性技术底座 | Consistent Self-Attention，热插拔进 SD1.5/SDXL | 6477 | Apache-2.0 |
| [ComicCrafter AI](tools/ai-comic-crafter.md) | 轻量漫画流水线 | Streamlit 单应用；单格定向修改不重生成整篇 | 4 | MIT（要 Gemini/ClipDrop key） |
| [comic-maker](tools/comic-maker.md) | 纯本地方案 | Ollama 写剧本→ComfyUI 画图→PIL 排版→导出 CBZ | 1 | MIT（⚠️早期项目） |
| [ComicStudio](tools/comic-studio.md) | 自主 Agent 虚拟工作室 | LangGraph：规划→对白→分镜→视觉质检→自动重画 | 4 | Apache-2.0（本地 SD 1.5） |
| [MangaNinja](tools/manganinja.md) | 线稿自动上色 | 参考图对色 + 点选指导 | 743 | ⚠️ CC BY-NC 4.0（非商用） |

## 决策树：我该用哪个

```
只是想玩一下，出一页漫画看看？
├─ 是 → AI Comic Factory（官网直接玩；仓库已归档，别自己搭）
├─ 要自己搭一条完整工作流？
│   ├─ 有 Gemini API → AI Comic Generator（JSON 驱动，角色三视图最完整）
│   │                    或 ComicCrafter AI（Streamlit 单文件，更轻）
│   └─ 坚决全本地 → comic-maker（Ollama+ComfyUI，1★ 早期项目）
│                    或 ComicStudio（LangGraph Agent + 本地 SD 1.5，自动化最高）
├─ 只解决"人物每格长得不一样"？
│       → StoryDiffusion（论文级方案，嵌进自己的 SD 管线）
└─ 手里有线稿，只想上色？
        → MangaNinja（CVPR 2025，参考图对色；注意非商用协议）
```

## 每家一页

- [AI Comic Factory](tools/ai-comic-factory.md) —— 一句话出整页漫画（已归档，官网体验）
- [AI Comic Generator](tools/ai-comic-generator.md) —— JSON 驱动，角色三视图 + 单格重画
- [StoryDiffusion](tools/story-diffusion.md) —— 人物一致性技术底座（NeurIPS 2024 Spotlight）
- [ComicCrafter AI](tools/ai-comic-crafter.md) —— 轻量 Streamlit，单格定向修改
- [comic-maker](tools/comic-maker.md) —— 纯本地全链路，导出 CBZ
- [ComicStudio](tools/comic-studio.md) —— 自主 Agent 虚拟漫画工作室
- [MangaNinja](tools/manganinja.md) —— 线稿自动上色（非商用协议注意）

## 共同前提

- 除了 StoryDiffusion / MangaNinja 两个论文实现，其余 5 家星数都很低（1–15★），属于"能用但别指望长期维护"
- 凡是要 Gemini / ClipDrop key 的，国内网络先解决再谈使用
- 评估日期 2026-10-19，star 数会变，选型时以仓库当前状态为准

## License

MIT
