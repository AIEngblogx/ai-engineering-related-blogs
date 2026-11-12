# AIEngblogx

把 Anthropic Engineering、Google DeepMind、OpenAI Engineering 的公开工程文章按段落排成中英对照，方便对着原文读术语。现在收了 70 篇。

站点在 https://aiengblogx.github.io/ai-engineering-related-blogs/，Pages 从 `main` 根目录发布。左边按来源分目录，顶部搜索中文英文都能搜；文章页中文在上、对应英文在下，点「隐藏英文原文」可以只留中文。每篇开头都有原文链接和日期。

译文只是帮着读，拿不准的地方以英文为准。译错了开个 issue，说哪篇哪段就行。

## 怎么生成的

这些 HTML 由 [AIEngblogx/AIEngblogx](https://github.com/AIEngblogx/AIEngblogx) 导出，别直接改生成物。抓取和翻译都在本机跑，文章数据不入库，换台机器得自己抓一遍：

```bash
npm ci
npm run build
node dist/main.js crawl --json
node dist/main.js translate --model <model> --lang zh-CN --json
node scripts/export-site.mjs ../ai-engineering-related-blogs https://aiengblogx.github.io/ai-engineering-related-blogs
```

第二个参数写进 RSS 链接，换域名时改这里重跑一次。只有有译文的文章会被导出。

## 版权

文章、译文和配图的权利归原作者，仓库里的 `LICENSE` 只管模板和脚本。哪家不希望自己的文章被收，开 issue，我会撤掉。
