# 网页设计优化 TODO

## 已完成

- [x] **#13** 修复 "Prepints" → "Preprints" 拼写错误（`my-publication.md`）
- [x] **#14** 导航栏 "关于我" → "About"（`_data/navigation.yml`）
- [x] **#15** 首页添加 tagline 摘要（`about.md`、`about-cn.md`）
- [x] **#16** 配色方案优化：primary `#7a8288` → `#1a365d`，link `#52adc8` → `#2b6cb0`（`_sass/_variables.scss`）
- [x] **#17** 教育背景 `&nbsp;` 硬编码缩进 → 嵌套列表（`about.md`、`about-cn.md`）
- [x] **#18** About 页面 section 间添加 `---` 分隔线（`about.md`、`about-cn.md`）
- [x] **#19** 按年份分组 Conference Papers（`my-publication.md`）
  - 将 9 篇论文按 2025 / 2024 / 2023 / 2020 / 2019 / 2018 分组展示，各组独立编号
- [x] **#20** 优化论文条目视觉层次
  - 在 `_sass/_page.scss` 中为 `.publication-list` 添加 CSS 样式
  - 用缩进、字重和颜色区分论文标题与会议/元信息
- [x] **#21** 优化移动端 Follow 按钮可见性
  - 在 `_sass/_sidebar.scss` 中增强 `btn--inverse` 样式
  - 添加主色调背景和阴影，使其在白色页面背景下更明显
- [x] **#22** 优化头像图片大小
  - `images/profile.png`（309KB）转为 `images/profile.webp`（6.1KB），尺寸缩至 350×442
  - 更新 `_config.yml` 中 `author.avatar` 路径为 `profile.webp`
- [x] **#23** 导航栏 About 链接改为英文首页（`_data/navigation.yml`）
  - `url: /about-cn/` → `url: /`
- [x] **#24** 添加中英文切换入口（`about.md`、`about-cn.md`）
  - 在页面顶部右侧添加语言切换链接
- [x] **#26** Google Analytics 迁移至 GA4（`_config.yml`）
  - `provider` 从 `google-universal` 改为 `google`
- [x] **#28** Open Graph 图片路径同步更新（`_config.yml`）
  - `og_image` 从 `profile.png` 改为 `profile.webp`
- [x] **#30** 清理模板残留文件
  - 删除 `_talks/2012-03-01-talk-1.md`、`_talks/2013-03-01-tutorial-1.md`
  - `_publications/` 中为真实论文，保留
- [x] **#31** 清理未使用的页面文件（`_pages/`）
  - 删除 `markdown.md`、`terms.md`
- [x] **#32** 移除 `.DS_Store` 并更新 `.gitignore`
  - 删除 `images/.DS_Store`，添加 `.DS_Store` 规则
- [x] **#33** 修复缺失的 Favicon（`images/`）
  - 从 `profile.webp` 生成全部 13 个 apple-touch-icon / favicon PNG 文件及 `favicon.ico`
- [x] **#34** 修复硬编码路径（`_includes/head/custom.html`、`_includes/footer/custom.html`）
  - favicon.ico 路径添加 `{{ base_path }}`，footer sitemap 链接添加 `{% include base_path %}`
- [x] **#36** 为主要页面添加 SEO meta description
  - 为 `about.md`、`about-cn.md`、`my-publication.md`、`awards.md`、`experiences.md`、`services.md`、`teaching.html` 添加描述性 excerpt
- [x] **#37** 添加多语言 hreflang 标签（`_includes/seo.html`）
  - 为 `/` 和 `/about-cn/` 添加 `rel="alternate" hreflang` 标签
- [x] **#38** 清理未使用的模板图片（`images/`）
  - 删除 13 个模板占位图和旧 profile 文件，减少约 700KB
  - 同步更新 `_data/authors.yml` 中 avatar 路径
- [x] **#39** 清理模板残留集合内容
  - 删除 `_portfolio/portfolio-1.md`、`portfolio-2.html`
- [x] **#40** 修复 Tongji URL 中的异常 `#/` 片段（`_pages/about.md`）
  - `https://en.tongji.edu.cn/p/#/` → `https://en.tongji.edu.cn/`
- [x] **#41** Follow 按钮改为 Contact（`_includes/author-profile.html`）
  - 按钮文字从无意义的 "Follow" 改为 "Contact"，保留展开社交链接的交互功能
- [x] **#42** Accessibility：teaser 图片 alt 属性（`_includes/archive-single.html`）
  - `alt=""` → `alt="{{ title }}"`，动态生成描述文字
- [x] **#43** 优化打印样式（`_sass/_print.scss`）
  - 添加字体大小调整、黑白配色、链接 URL 显示、分页规则、孤行寡行控制
- [x] **#44** 补充 `.gitignore` 规则
  - 添加 `.sass-cache/`、`.jekyll-cache/`、`.jekyll-metadata`、`.bundle/`、`node_modules/`
- [x] **#45** 启用面包屑导航（`_config.yml`）
  - `breadcrumbs: false` → `breadcrumbs: true`

## 待完成（需人工操作）

- [ ] **#25** 评估 Blog 外链去留（`_data/navigation.yml`）
  - 当前链接指向 `https://vincent27hugh.github.io/`（另一个仓库）
  - 若不再维护，建议移除导航项；若仍活跃，保持现状

- [ ] **#27** 配置搜索引擎验证（`_config.yml`）
  - `google_site_verification` 当前为空，影响 Google 索引
  - 需在 Google Search Console 中获取验证码并填入

- [ ] **#29** 优化宽屏阅读体验（`_sass/_variables.scss`）
  - 右侧边栏宽度全部设为 `0px`；内容已有 `max-width: 1280px` 限制
  - 如需进一步优化可恢复适当侧边栏宽度

- [ ] **#35** 更新 CV 文件（`files/`）
  - CV PDF 日期为 2023 年，但简历已显示 2024.07 至今的特聘研究员职位
  - 需用户提供更新后的 PDF 文件

## 涉及文件汇总

| 文件 | 改动项 |
|------|--------|
| `_pages/my-publication.md` | #13, #19, #36 |
| `_data/navigation.yml` | #14, #23, #25 |
| `_data/authors.yml` | #38 |
| `_pages/about.md` | #15, #17, #18, #23, #24, #36, #40 |
| `_pages/about-cn.md` | #15, #17, #18, #24, #36 |
| `_pages/awards.md` | #36 |
| `_pages/experiences.md` | #36 |
| `_pages/services.md` | #36 |
| `_pages/teaching.html` | #36 |
| `_sass/_variables.scss` | #16, #29 |
| `_sass/_page.scss` | #20 |
| `_sass/_sidebar.scss` | #21 |
| `_sass/_print.scss` | #43 |
| `images/` (favicon 生成) | #33 |
| `images/` (模板图片清理) | #22, #38 |
| `_config.yml` | #22, #26, #27, #28, #45 |
| `_includes/head/custom.html` | #33, #34 |
| `_includes/footer/custom.html` | #34 |
| `_includes/seo.html` | #37 |
| `_includes/author-profile.html` | #41 |
| `_includes/archive-single.html` | #42 |
| `files/` (CV PDFs) | #35 |
| `_talks/*.md` | #30 |
| `_portfolio/*.md` / `*.html` | #39 |
| `_pages/markdown.md`、`terms.md` | #31 |
| `.gitignore` | #32, #44 |
