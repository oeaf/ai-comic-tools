# AI Comic Generator

https://github.com/Dapeng960208/AI-Comic-Generator · 15 star · MIT · 维护中

## 一句话

JSON 驱动的完整漫画工作流：故事→分镜脚本→角色设定（三视图）→逐格生成→单格重画，全套管够。

## 怎么玩

- 技术栈：FastAPI + SQLite 后端，Vue 3 + Element Plus 前端，前后端都要起
- 核心设计是"一切皆 JSON"：故事大纲、角色设定、分镜细节全是结构化数据，方便版本管理和接 AI
- 角色一致性：自动从故事里抽角色、生成三视图设定，画分镜时用设定图做 img2img 参考
- 全局风格配置：画风/画幅/配色/对话框样式一次定义，自动同步到所有分镜
- 后台任务：批量画图扔后台跑，前端看进度

## 适合谁

- 想认真做连载感漫画、需要角色长期稳定的人：三视图 + 全局风格是这 7 家里最完整的一套
- 开发者：JSON 驱动的设计方便二次开发

## 注意

- **强依赖 Google Gemini**：文本用 `gemini-3-flash-preview`，画图用 `gemini-3-pro-image-preview`，必须有 Google Cloud API Key
- 国内网络直连 Gemini 是个坎，用之前先解决网络和 key
- 15 star 的小项目，issue 响应别抱太高期望
