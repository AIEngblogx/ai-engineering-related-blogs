# AIEngblogx

AI 工程博客的中英对照阅读站，按段落对齐原文与译文。收录 Anthropic Engineering、Google DeepMind、OpenAI Engineering 的公开文章，目前 61 篇。

站点：https://aiengblogx.github.io/ai-engineering-related-blogs/（GitHub Pages，从 `main` 根目录发布）。侧边栏按来源分组、可折叠；文章页支持全文检索与隐藏英文原文。译文以英文原文为准。

## 生成

页面由 [AIEngblogx/AIEngblogx](https://github.com/AIEngblogx/AIEngblogx) 导出，抓取、翻译与生成在本机完成，文章数据不入库。

```bash
npm ci
npm run build
node dist/main.js crawl --json
node dist/main.js translate --model <model> --lang zh-CN --json
node scripts/translate-titles.mjs <model>
node scripts/export-site.mjs ../ai-engineering-related-blogs https://aiengblogx.github.io/ai-engineering-related-blogs
```

第二个参数是站点 URL，写入 RSS 链接。导出只收录有译文且正文完整的文章，并清理上一版不再收录的页面。

## 版权

文章、译文与配图权利归原作者。仓库 `LICENSE` 覆盖模板、样式与脚本。勘误与下架请求通过仓库 Issue 提交。
