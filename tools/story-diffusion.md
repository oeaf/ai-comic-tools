# StoryDiffusion

https://github.com/HVision-NKU/StoryDiffusion · 6477 star · Apache-2.0 · NeurIPS 2024 Spotlight 论文官方实现

## 一句话

解决"AI 连画好几张、人物每张长得不一样"的自注意力技术：一次生成长序列形象一致的图片/视频，热插拔进任何 SD1.5 / SDXL 模型。

## 怎么玩

- 这是**技术底座**，不是开箱即用的漫画 App：给你 Consistent Self-Attention 模块，接到自己的 SD 管线里
- 最少 3 个 prompt 起用，推荐 5–6 个，排版效果更好
- 另带一个 motion predictor：拿一致性图片再做长视频，两段式
- 想先看效果：[Hugging Face Space 漫画 demo](https://huggingface.co/spaces/YupengZhou/StoryDiffusion) / Colab / Replicate 都有现成入口

## 适合谁

- 已经在用 SD1.5/SDXL 做图、被人物一致性折磨的人：这是 7 家里唯一的论文级解法
- 做 AI 漫画/短剧工作流的开发者：拿它当一致性模块嵌入自己的管线

## 注意

- 代码 Apache-2.0 可商用，但底座 SD 模型本身走 CreativeML Open RAIL-M，商用前看一眼模型授权
- 需要本地 GPU 跑扩散模型；纯想要"点几下出漫画"的人别选它
