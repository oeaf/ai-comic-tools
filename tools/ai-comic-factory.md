# AI Comic Factory

https://github.com/jbilcke-hf/ai-comic-factory · 1349 star · Apache-2.0 · ⚠️ 2025-10-31 已归档为只读

## 一句话

一句话故事描述 + 选画风，直接出一整页漫画：LLM 写分镜脚本，SDXL 负责画图。AI 漫画工具里的"祖师爷"级 demo。

## 怎么玩

- 最省事：官网 [aicomicfactory.app](https://aicomicfactory.app) 直接玩，不用部署
- 自己搭：仓库是 Hugging Face Space（Docker），但不是单体可复制——前端/后端/LLM/SDXL 要分开配
- 自部署要准备一堆 key：`LLM_ENGINE`（HF/OpenAI/Groq/Anthropic 四选一）+ `RENDERING_ENGINE`（HF/Replicate/VideoChain/OpenAI），`.env` 里逐项填

## 适合谁

- 只想体验"一句话变漫画"：走官网，别碰仓库
- 想抄它的流水线设计：LLM 分镜 + SDXL 画图这套分工值得借鉴

## 注意

- **仓库已归档只读**，不会再更新；SDXL 是 2023 年的技术，画质别跟现在的模型比
- 自部署配置繁琐，单纯想用的人直接官网
