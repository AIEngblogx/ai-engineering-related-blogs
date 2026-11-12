# AIEngblogx

公开 AI 工程博客的中英对照阅读站，目前收录 28 篇，持续补充。页面由工具仓库生成，可直接用 GitHub Pages 托管。

## 部署

1. 仓库 Settings → Pages → Deploy from a branch → `main` / `(root)`。
2. 站点地址：`https://aiengblogx.github.io/ai-engineering-related-blogs/`。
3. 若实际地址不同，重新导出时把它作为第二个参数传入，以修正 RSS 链接。

## 内容

| 路径 | 内容 |
|---|---|
| `index.html` | 书目录（按来源分组的左侧目录、顶部全文搜索、篇末翻页） |
| `viewers/*.html` | 文章页，逐段中英对照（可切换隐藏英文原文）、原文配图、原文链接与日期 |
| `about.html` | 声明、搜索、主题与版权说明 |
| `search-index.json` | 全文搜索用的倒排索引，首次搜索时加载 |
| `rss.xml` | 订阅 |

## 站点生成

页面由 [AIEngblogx/AIEngblogx](https://github.com/AIEngblogx/AIEngblogx) 的
`scripts/export-site.mjs` 从抓取数据生成，请勿手工编辑 HTML。工具仓库只包含代码；
文章数据留在本机，不入库。复现步骤见工具仓库 README 与 CONTRIBUTING。
只有已完成译文的文章会被导出。

## 版权与内容

文章正文、译文与配图的权利归原作者所有，本仓库 `LICENSE` 只覆盖页面模板、样式与脚本。
本站为非官方归档，每篇保留原文链接与发布日期；中文译文仅作辅助阅读，请以英文原文为准。
如需下架某篇或修正译文，请在本仓库提交 Issue，注明文章链接与原因。
