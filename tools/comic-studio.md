# ComicStudio

https://github.com/CallmeTruong/Comic_Studio · 4 star · Apache-2.0 · 维护中

## 一句话

一个 LangGraph 自主 Agent 扮演**完整虚拟漫画工作室**：故事规划→写对白→画分镜→视觉质检→缺失元素自动重画，全程不用你盯。

## 怎么玩

- Agent 工作流：Story Planner（故事节拍+角色设定）→ Dialogue Writer（英文/越南语对白）→ Storyboarder（分镜）→ Art Director 校验 → SD 1.5 本地渲染 → Vision QA（拿成图检查缺人/缺道具/穿帮）→ 不合格自动打回重画（最多 3 轮）
- 长 prompt 用 Compel 分块加权，不会悄悄截断
- 页面排版自动或仿 manga 版式，对话框后加上去；每格可单独改图或改对白
- UI 实时推送 planner/renderer/QA 的进度事件

## 适合谁

- 想体验"Agent 自己把漫画从头做到尾"的人：这 7 家里自动化程度最高的
- 本地有 SD 1.5 环境、不想调云 API 的人

## 注意

- 4 star 早期项目；对白只支持英文/越南语，中文对白要自己接
- Vision QA 那一步要调视觉模型，本地/云端二选一，提前规划成本
