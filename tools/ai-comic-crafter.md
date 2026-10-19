# ComicCrafter AI

https://github.com/Balajee2k/AI-Comic-Crafter · 4 star · MIT · 维护中

## 一句话

故事变连环漫画的轻量流水线（Streamlit 单文件应用）：核心卖点是**只改不满意的那一格**，不用整篇重生成。

## 怎么玩

- `pip install` + `streamlit run` 即起，6 种精选风格：日式 Manga、Anime、美式超级英雄、欧漫 ligne claire、竖屏 Webtoon、黑电影
- Session memory：跟它说"第 3 格把对白改成……"，只重画那一格，其余不动
- 角色一致性靠参考图 + prompt 注入；情绪感知排版（分镜大小/边框/色温跟着剧情走）
- 导出 PNG / PDF / 单格

## 适合谁

- 想要 AI Comic Generator 的"单格修改"能力，但嫌前后端太重的人：这个一个 Streamlit 就够
- 风格要现成可靠的：6 种是精挑过"跨格稳定"的

## 注意

- 依赖 Google Gemini（故事）+ ClipDrop / Stability AI（画图），都要 key
- 4 star 早期项目，4 种风格之外的需求自己改代码
