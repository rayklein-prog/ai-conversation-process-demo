# 寻知 AI 对话过程演示

这是一个无需安装依赖的静态 HTML 原型，用于展示智能体执行过程的状态编组、异常外显、子任务展开、流式回答和滚动接管交互。

## 在线预览

[在线打开 Demo](https://rayklein-prog.github.io/ai-conversation-process-demo/)。GitHub Actions 会发布 `public-release/` 目录。

## 过程加载怎么阅读

- 处理时只外显进度文本、当前操作和异常；连续的普通操作会合并成一个可展开的组。
- 多项操作运行时显示最新动作，结束后会按内容概括，例如“已完成资料读取与校验（4 项）”；只有一项时直接显示，不再重复套组。
- 失败、超时、停止和等待确认始终外显，避免重要状态被收起。
- 点开任意过程详情会暂停自动追随；点击输入框上方的圆形提示，或手动滚回底部，才会继续跟随新内容。
- 过程完成后会自动收起，正文从开头流式输出，并由用户自行滚动阅读。

完整的状态、编组、动效和事件接入约定见 [过程加载与交互规则.md](过程加载与交互规则.md)。

## 本地打开

直接用浏览器打开 [ai-conversation.html](ai-conversation.html)，或启动任意静态文件服务并访问该文件。

## 目录

- `ai-conversation.html`：可编辑的单文件源码。
- `index.html`：内嵌形象素材的独立预览副本。
- `public-release/`：GitHub Pages 实际发布内容。
- `assets/figma/`：Figma 导出的图标和形象素材。
- [过程加载与交互规则.md](过程加载与交互规则.md)：过程状态、编组、滚动、加载提示与事件协议。
- `AI-CONVERSATION-README.md`：设计对齐和原型背景记录。

## 发布规则

推送到 `main` 后，GitHub Actions 将 `public-release/` 部署到 Pages。更新页面时，同步 `ai-conversation.html` 到 `public-release/index.html`，再推送即可。
