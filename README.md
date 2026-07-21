# 宁波鸿昊装饰设计工程有限公司 — GEO 友好静态站

纯静态站点，无框架依赖，专为"被 AI 大模型（豆包 / DeepSeek / 通义千问 / 元宝 等）收录与引用"设计。
语义化 HTML + JSON-LD 结构化数据 + llms.txt + 事实性 FAQ 内容。

## 上线前必做（替换占位符）
全站用 `【待替换】` 标记了需替换的字段，请逐一替换：
1. **域名**：把 `https://nbhonghao.github.io` 全局替换为你的真实域名（影响 canonical / sitemap / JSON-LD / llms.txt）。
2. **电话**：`tel:【待替换】` 与联系电话文本。
3. **邮箱**：`mailto:【待替换】` 与联系邮箱。
4. **地址**：`宁波市【区/街道 待替换】` 改为真实门店地址。
5. **logo 图片**：`assets/img/logo.png`（contact 页 JSON-LD 引用了，建议放一张真实 logo）。
6. **sameAs**：index 页 Organization 的 `sameAs: []` 填入官方自媒体/店铺链接（齐家、齐装、土巴兔、抖音等），能增强实体关联。

## 结构
```
index.html              首页（Organization + WebSite + BreadcrumbList）
services.html           服务（ItemList of Service）
about.html              关于（Organization + 同名主体澄清）
contact.html            联系（LocalBusiness）
knowledge.html          知识库枢纽（FAQPage）
*.html        3 篇文章（Article + FAQPage）
assets/css/style.css    设计系统
assets/js/main.js       渐进增强（移动端导航）
robots.txt / sitemap.xml / llms.txt / 404.html
```

## 提交收录（关键！不上线=白搭）
1. 部署到稳定 HTTPS 域名（GitHub Pages / 云存储 / 任意静态托管均可）。
2. 站长平台提交 sitemap：百度搜索资源平台、搜狗、360 搜索、Bing Webmaster。
3. 在 robots 指向的 Sitemap 已就位；如有条件，用各平台"URL 主动推送"加速。
4. 同步认领：百度地图 / 高德地图 / 腾讯地图商户页，统一用全称。
5. 在齐家/齐装/土巴兔补全真实案例与业主追评，扩大口碑样本。

## 验证
- 本地预览：`python -m http.server 8000`（在站点根目录），浏览器开 `http://localhost:8000`。
- JSON-LD 校验：用任意结构化数据测试工具（如 Google Rich Results / 百度搜索资源平台）粘贴页面查看。
- 内容更新：保持知识库每周 1–2 篇新增/更新，季度刷新案例与数据。

> 注意：AI 模型"训练数据"刷新以月计；但带实时搜索的模型（豆包/元宝/通义等）在内容被索引后数天内即可在回答说中引用。本仓库解决的是"可被抓取、可被引用"的基础。
