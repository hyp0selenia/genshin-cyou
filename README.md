# 原神启动复刻 · Cloudflare Workers

基于原项目改造：https://github.com/gamemcu/www-genshin

## GitHub 部署

将本目录所有文件推送到 GitHub，在 Cloudflare 的 Workers & Pages 中连接该仓库，设置：

- 根目录：`/`
- 构建命令：`npm ci && npm run build`
- 部署命令：`npx wrangler deploy`
- 生产分支：选择仓库的生产分支（例如 `main`）

`wrangler.jsonc` 指定 Worker 入口和静态资源目录；Cloudflare 会在构建时生成 `dist/`。

## 本地预览

使用 Node.js 22：

```sh
npm ci
npm run build
npx wrangler dev
```
