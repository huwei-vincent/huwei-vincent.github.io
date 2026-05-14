# 网页设计优化 TODO

## 已完成

- [x] **#13** 修复 "Prepints" → "Preprints" 拼写错误（`my-publication.md`）
- [x] **#14** 导航栏 "关于我" → "About"（`_data/navigation.yml`）
- [x] **#15** 首页添加 tagline 摘要（`about.md`、`about-cn.md`）
- [x] **#16** 配色方案优化：primary `#7a8288` → `#1a365d`，link `#52adc8` → `#2b6cb0`（`_sass/_variables.scss`）
- [x] **#17** 教育背景 `&nbsp;` 硬编码缩进 → 嵌套列表（`about.md`、`about-cn.md`）
- [x] **#18** About 页面 section 间添加 `---` 分隔线（`about.md`、`about-cn.md`）

## 待完成

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

## 涉及文件汇总

| 文件 | 改动项 |
|------|--------|
| `_pages/my-publication.md` | #13, #19 |
| `_data/navigation.yml` | #14 |
| `_pages/about.md` | #15, #17, #18 |
| `_pages/about-cn.md` | #15, #17, #18 |
| `_sass/_variables.scss` | #16 |
| `_sass/_page.scss` | #20 |
| `_sass/_sidebar.scss` | #21 |
| `images/profile.png` | #22 |
| `_config.yml` | #22 |
