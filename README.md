# AI 脑图空间站 (AI-Mindmap)

> 别人在追热点，你已经在看全貌。

一张交互式 AI 知识地图，涵盖 150+ AI 核心概念（147 节点），每个节点可展开关联概念、做笔记、收藏，并内置 AI 问答深度探索。

## 特点

- **零后端**：纯静态站点，数据全部内嵌，笔记/收藏/对话记录存用户浏览器 localStorage
- **AI 问答自带 Key**：用户配置自己的 OpenAI 兼容 API（火山方舟/DeepSeek/智谱等均可），Key 只存本地不上传
- **交互式导图**：拖拽缩放、节点路径导航、选中文字提问、历史对话搜索

## 使用

直接打开 `index.html` 即可（或访问 GitHub Pages 地址）。

AI 问答首次使用需配置 API Key：点击聊天面板右上角 ⚙️，免费 Key 获取教程见 [api-guide.html](api-guide.html)。

## 技术说明

- 单文件应用：`index.html`（数据内嵌 + 原生 JS）
- AI 调用：OpenAI 兼容 `/chat/completions`，SSE 流式响应
- 本地存储：localStorage（`ai_note_*` 笔记 / `ai_favs_*` 收藏 / `ai_api_config` API 配置）

## 历史版本

- v6.x（2026-05~08）：Express + Redis + 登录体系（服务器版）
- 本版（2026-11）：去服务器化，GitHub Pages 零成本运行
