# comic-maker

https://github.com/AskAillex/comic-maker · 1 star · MIT · ⚠️ 早期开发中（作者边做边开源）

## 一句话

**完全本地**的一句话变漫画：Ollama 写剧本 → ComfyUI 画分镜 → PIL 排版（对话框/SFX/斜切分镜/标题条），最后导出 CBZ，不花一分钱、不用任何账号。

## 怎么玩

```bash
python comicify.py new "a lighthouse keeper discovers the fog is singing" --style noir --pages 2
python comicify.py all a_lighthouse_keeper_discovers_th
```

- 前置：Python 3.10+、Ollama（任意 chat 模型）、ComfyUI（z-image turbo 检查点）
- 角色一致性：同一角色用同一种子家族 + 每格重述完整外貌描述
- 4 种内置风格：sunday-strip / manga / noir / euro-album，也可传任意风格描述
- 各阶段可独立跑：`script` → 手改 `script.json` → `panels` → `assemble`

## 适合谁

- 坚决不上云、机器上有显卡的人：这 7 家里唯一的纯本地全链路
- 想学"AI 自己开漫画工作室"玩法的：作者的 Aillex 项目就是拿它日更的

## 注意

- 作者明示"API、prompt、排版都还会变"，当半成品用
- 风格描述里别放可画出来的实词（比如 "sunday"），模型会真的画进图里——作者踩过的坑
- 1 star，基本是作者自用项目，文档和 issue 都别指望
