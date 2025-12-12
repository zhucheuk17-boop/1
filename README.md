# Campus Rose Competition (Demo)

This repository contains a simple static site `index.html` (Campus Rose Competition - Garden Club demo). The repo is minimal; use the instructions below to preview the HTML locally.

## How to run

- Using Python built-in HTTP server (no Node required):

```bash
# From repository root
python3 -m http.server 8000
# Then open http://localhost:8000/index.html in your browser
```

- Using Node.js (npx http-server):

```bash
npm install # optional
npm start
# Default script runs: npx http-server -p 8080
# Then open http://localhost:8080/index.html
```

- Using Docker + nginx (static file hosting):

```bash
docker run --rm -it -v "$PWD":/usr/share/nginx/html:ro -p 8080:80 nginx:alpine
# Then open http://localhost:8080/index.html
```

- VS Code Live Server: install the Live Server extension, open `index.html`, and click "Go Live".

## Notes

- This is a static demo with inline CSS and JS (no build step).
- If you prefer, I can scaffold a small Node or Python project with tests and CI.

## GitHub Pages (自动部署)

已添加 GitHub Actions 流程来部署静态站点到 GitHub Pages。当你把内容推送到 `main` 分支时，Actions 会将 `index.html` 与其他静态文件打包并部署到 Pages。

部署触发器：
- Push 到 `main` 分支；或在 Actions -> Deploy to GitHub Pages -> Run workflow 手动触发。

部署后站点地址（默认）：
`https://<GitHub用户名>.github.io/1/`

示例：
`https://zhucheuk17-boop.github.io/1/`

注意：首次部署后，有时 GitHub Pages 需要几分钟来准备站点；如果想在生产环境长期托管，推荐使用 GitHub Pages、Netlify 或 Vercel 等托管服务。