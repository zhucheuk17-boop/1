<!--
This file guides AI coding agents (e.g., Copilot, internal coding agents) on how to be useful in this repository.
Keep instructions concise, actionable, and grounded in the discoverable code and repository layout.
-->

# Copilot / AI Agent Instructions

仓库当前非常精简 —— 只有根目录下的 `index.html`。因此本指南优先说明如何在空仓库/最小项目上工作，以及在本仓库中实现常见约定时应遵循的明确、可执行规则。

1. 识别语言与架构
- 如果仓库只包含 `index.html`，请先询问用户是否想要将项目扩展为真实应用（例如添加 Node/Python/Rust Web 框架）。

2. 约定目录结构（若无则建议）
- `src/`：主实现代码放置位置。
- `tests/`：单元/集成测试。
- `docs/`：设计或 API 文档。
- `.github/workflows/`：CI 配置（已添加 Pages 自动部署示例）。

3. 开发工作流与命令
- 目前该仓库为静态页面，推荐以下本地测试方式：
  - Python 内建服务器：`python3 -m http.server 8000`
  - Node.js：`npm start`（在 `package.json` 中已定义 `start` 脚本）

4. PR 与提交习惯
- 使用小而单一目的的提交与 PR（一个 PR = 一个功能或修复）。
 
5. 自动化与 CI
- 本仓库已添加 `.github/workflows/pages.yml`，自动部署到 GitHub Pages。修改后触发 action 部署站点。

6. 与 AI 合作的具体行为
- 在仓库无明确线索时，先询问用户首选技术栈或任务目标（例如：实现 API、搭建 CLI、加测试）。

7. 安全与边界条件
- 不要将敏感信息（例如权限 token、密钥）写入仓库；优先使用 Actions secrets 和 .env 文件。

8. 迁移或增量更改的指南
- 对于新增约定（如 monorepo 或 CI），优先创建 `docs/` 下的 ADR（Architecture Decision Record）。
