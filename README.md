# ZJUT AI 宣传部 · 素材页

一句话：**做推文，素材从协会公开仓库拿。** 这一页只有一个按钮——复制提示词，交给 AI 去仓库里找。

## 文件

```
index.html    单页，零依赖，双击即看；4.7 KB
```

## 页面上有什么

| 元素 | 内容 |
| :--- | :--- |
| 标题 | 做推文，素材从这个仓库拿。 |
| 一句话 | 协会的 logo、配色、怎么用，都写在里面。不用下载、不用转存，也不用问人要图。 |
| 主按钮 | 复制提示词（提示词藏在 `id="prompt"` 的 `<pre>` 里，改流程只改那一段） |
| 文字链接 | 打开仓库 → `github.com/Ljh15224052032/zjutai-brand` |

规范本身**不抄到页面上**，只在仓库里维护一份（`README.md` + `guidelines.md`）。页面写得越少，越不会过期。

## 为什么这么简

素材怎么用、用哪版 logo、配色多少，仓库里已经有了。页面上再写一遍就是第二份真相，改一处忘一处。

## 放出去

已上线：**https://brand.zjutai.cn**（Cloudflare Pages，项目 `zjut-brand`，静态，不占服务器）

重新部署（本机 wrangler 在官网项目里）：

```bash
node D:/Code-Rebuild/1-projects/ZJUTAI-官网/tools/node_modules/wrangler/bin/wrangler.js \
  pages deploy D:/Code-Rebuild/1-projects/zjutai-workbench \
  --project-name=zjut-brand --branch=main
```

需要环境变量 `CLOUDFLARE_API_TOKEN`（见 `D:\AI-task\API密钥.md` 的 Cloudflare 一节）和 `CLOUDFLARE_ACCOUNT_ID`。

坑：用 API 绑定自定义域时，**Cloudflare 不会自动建 DNS**，要手动加一条 CNAME `brand → zjut-brand.pages.dev`（开代理），否则域一直卡在 pending。

**不要部署到 `8.217.72.150`**：个人博客机，不对外给宣传部用。

## 以后可能加什么

推文模板仓库。等成品攒够、仓库建好，在「打开仓库」旁边加第二个链接就够，不要再长出一堆卡片。
