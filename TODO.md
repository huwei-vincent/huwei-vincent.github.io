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

- [x] **#46** 前端 UI 深度优化（多个 SCSS 文件）
  - 排版：body `line-height` 1.5→1.6，标题 `margin-top` 2em→1.5em，h5/h6 字号区分（`_base.scss`）
  - 颜色：链接色 `#2b6cb0`→`#1a5490` 提升对比度，footer 文字从近白改为 `$gray`（`_variables.scss`、`_footer.scss`）
  - 间距：主容器 `margin-top` 2em→1.5em，masthead padding 增至 1.2em（`_page.scss`、`_masthead.scss`）
  - 视觉：头像添加 `box-shadow`，`border-radius` 4px→6px，表格行 hover 高亮（`_sidebar.scss`、`_variables.scss`、`_tables.scss`）
  - 导航：面包屑添加浅灰背景和底部边框（`_navigation.scss`）
  - 编码：`main.scss` 添加 `@charset "utf-8"` 防止 SCSS 编译错误

- [x] **#47** 导航栏排序优化（`_data/navigation.yml`）
  - Research → Awards → Teaching → Experiences → Services → CV

- [x] **#48** ~~首页快速导航卡片~~ — **已移除**（与导航栏功能重复）

- [x] **#49** Services 页面按会议层级分组（`services.md`）
  - Conference Review 分为 "Premier IS Conferences"（ICIS, PACIS, CIST）和 "Specialized Conferences"

- [x] **#50** Awards 页面按类别分组（`awards.md`）
  - 分为 Teaching & Research Excellence / University Recognition / Competition Awards / Scholarships

- [x] **#51** Experiences 页面时间线布局（`experiences.md`、`_sass/_page.scss`）
  - 使用 `.timeline` 组件，添加年份标记和圆点装饰的垂直时间线

- [x] **#52** ~~论文摘要可展开/折叠~~ — **已移除**（用户决定不添加）

- [x] **#53** CV 页面增强（`cv.md`、`_sass/_page.scss`）
  - 添加 "At a Glance" 简要信息块
  - 下载链接改为主色调按钮样式

- [x] **#54** 深色/浅色主题切换（`_sass/_dark-mode.scss`、`_includes/masthead.html`、`_includes/head/custom.html`、`_includes/footer/custom.html`）
  - 新增 `_sass/_dark-mode.scss`：完整深色主题变量与样式覆盖
  - 导航栏添加 SVG 月亮/太阳切换按钮（放在 `nav` 外避免 greedy-nav JS 吞掉）
  - `localStorage` 持久化用户偏好，自动跟随系统 `prefers-color-scheme`
  - `head/custom.html` 添加预渲染脚本防止白屏闪烁
  - 打印时强制浅色模式，隐藏切换按钮

- [x] **#55** 跨平台适配优化（`_sass/_dark-mode.scss`、`_sass/_page.scss`、`_sass/_masthead.scss`）
  - 切换按钮从 emoji（🌙/☀️）改为 SVG 图标（Feather Icons），跨平台渲染一致
  - 切换按钮最小触控区域 44×44px（WCAG 标准）
  - Flexbox 添加 `-webkit-`、`-ms-` 前缀兼容旧浏览器
  - `gap` 属性添加 `margin` fallback 兼容 Safari < 14.1
  - 时间线 ≤600px 切换纵向排列，CV 按钮 ≤400px 纵向堆叠
  - 导航栏 `masthead__inner-wrap` 添加 `position: relative` + 右侧留白避免按钮重叠
  - 键盘导航 `:focus` 轮廓 + `:focus:not(:focus-visible)` 隐藏鼠标点击轮廓

## 待完成（需人工操作）

- [x] **#25** 评估 Blog 外链去留（`_data/navigation.yml`）
  - 保留现有外链 `https://vincent27hugh.github.io/`

- [x] **#27** 配置搜索引擎验证（`_config.yml`）
  - 已填入 Google Search Console 验证码

- [x] **#29** 优化宽屏阅读体验（`_sass/_variables.scss`）
  - 右侧边栏宽度从 `0px` 恢复为 `100px / 150px / 200px`（narrow / normal / wide）
  - 为宽屏增加右侧留白，缩短文本行宽，提升阅读舒适度

- [ ] **#35** 更新 CV 文件（`files/`）— **暂停，待后续处理**
  - CV PDF 日期为 2023 年，但简历已显示 2024.07 至今的特聘研究员职位
  - 需用户提供更新后的 PDF 文件

## 涉及文件汇总

| 文件 | 改动项 |
|------|--------|
| `_pages/my-publication.md` | #13, #19, #36 |
| `_data/navigation.yml` | #14, #23, #25, #47 |
| `_data/authors.yml` | #38 |
| `_pages/about.md` | #15, #17, #18, #23, #24, #36, #40 |
| `_pages/about-cn.md` | #15, #17, #18, #24, #36 |
| `_pages/awards.md` | #36, #50 |
| `_pages/experiences.md` | #36, #51 |
| `_pages/services.md` | #36, #49 |
| `_pages/cv.md` | #53 |
| `_pages/teaching.html` | #36 |
| `_sass/_variables.scss` | #16, #29 |
| `_sass/_page.scss` | #20, #51, #53, #55 |
| `_sass/_dark-mode.scss` | #54, #55 |
| `_sass/_sidebar.scss` | #21 |
| `_sass/_masthead.scss` | #46, #55 |
| `_sass/_print.scss` | #43 |
| `assets/css/main.scss` | #46, #54 |
| `images/` (favicon 生成) | #33 |
| `images/` (模板图片清理) | #22, #38 |
| `_config.yml` | #22, #26, #27, #28, #45 |
| `_includes/head/custom.html` | #33, #34, #54 |
| `_includes/footer/custom.html` | #34, #54 |
| `_includes/masthead.html` | #54, #55 |
| `_includes/seo.html` | #37 |
| `_includes/author-profile.html` | #41 |
| `_includes/archive-single.html` | #42 |
| `files/` (CV PDFs) | #35 |
| `_talks/*.md` | #30 |
| `_portfolio/*.md` / `*.html` | #39 |
| `_pages/markdown.md`、`terms.md` | #31 |
| `.gitignore` | #32, #44 |
