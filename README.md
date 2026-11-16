# AIEngblogx

收录 AI 实验室公开工程文章中关于怎么用 AI、以及 AI 系统原理的内容，按段落对齐中文译文与英文原文。目前 96 篇，来自 Anthropic Engineering、Cohere Blog、Google DeepMind、OpenAI Engineering。

站点：[GitHub Pages](https://aiengblogx.github.io/ai-engineering-related-blogs/) · [站点仓库](https://github.com/AIEngblogx/ai-engineering-related-blogs) · [工具仓库](https://github.com/AIEngblogx/AIEngblogx)

## 生成

页面由 [AIEngblogx/AIEngblogx](https://github.com/AIEngblogx/AIEngblogx) 的 `scripts/export-site.mjs` 从本机抓取数据导出，文章数据不入库。

```bash
npm ci
npm run build
node dist/main.js crawl --json
node dist/main.js translate --model <model> --lang zh-CN --json
node scripts/translate-titles.mjs <model>
node scripts/export-site.mjs ../ai-engineering-related-blogs https://aiengblogx.github.io/ai-engineering-related-blogs/
```

第二个参数是站点 URL，用于生成 RSS 绝对链接。导出只收录译文完整且正文不少于 3 段的文章，并清理上一版不再收录的页面。

## 版权

文章、译文与配图权利归原作者，以英文原文为准。`LICENSE` 仅覆盖页面模板、样式与脚本。勘误与下架请求通过仓库 Issue 提交。
