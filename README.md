# 寻知 AI 对话过程演示

这是一个无需安装依赖的静态 HTML 原型，用于展示智能体执行过程的状态编组、异常外显、子任务展开、流式回答和滚动接管交互。

## 在线预览

启用 GitHub Pages 后，仓库首页的 **Deployments** 会显示最新预览地址。GitHub Actions 会发布 `public-release/` 目录。

## 本地打开

直接用浏览器打开 [ai-conversation.html](ai-conversation.html)，或启动任意静态文件服务并访问该文件。

## 目录

- `ai-conversation.html`：可编辑的单文件源码。
- `index.html`：内嵌形象素材的独立预览副本。
- `public-release/`：GitHub Pages 实际发布内容。
- `assets/figma/`：Figma 导出的图标和形象素材。
- `PROCESS-LOADING-SPEC.md`：过程状态、编组、滚动、加载提示与事件协议。
- `AI-CONVERSATION-README.md`：设计对齐和原型背景记录。

## 发布规则

推送到 `main` 后，GitHub Actions 将 `public-release/` 部署到 Pages。更新页面时，同步 `ai-conversation.html` 到 `public-release/index.html`，再推送即可。
