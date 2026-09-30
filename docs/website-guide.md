# 网站维护

当前沿用英文网站。四个主菜单分别为 About、Event、Team、Join us；Event 下有 Upcoming 和 Past，因此共有五个主要页面。

## 页面位置

- About 首页：`content/_index.md`；介绍文案在 `layouts/partials/forum.html`。
- Upcoming：`content/event/_index.md`，网址 `/event/`。
- Past：`content/event/past/index.md`，网址 `/event/past/`。
- Team：`content/team/index.md`；组织者资料在 `data/organizers.yaml`，照片在 `static/images/`。可增加 `affiliation` 和 `bio` 字段。
- Join us：`content/contact/index.md`；联系邮箱在 `layouts/partials/forum.html`。
- Logo：直接使用原始 `assets/media/logo.png`，保留比例，不重新绘制。
- 视觉：白底、黑灰正文、蓝色链接；不使用装饰性渐变、轨道插图或宣传口号。
- 菜单：`config/_default/menus.yaml`；样式：`static/css/forum.css`。

团队已更新为十位组织者，并按姓氏字母顺序排列；职称、单位、研究方向和来源链接保存在 `data/organizers.yaml`，官方照片保存在 `static/images/team/`。复旦两位成员的“青年研究员”保留官网原职称，不自行换算为 Assistant Professor。联系邮箱按组织者要求暂设为 `omics4health@gmail.com`（占位地址，未验证是否启用）。旧示例讲座和示例新闻已设为草稿，未删除源文件。

## 添加讲座

新建 `content/event/讲座英文短名/index.md`，按以下格式填写。以下仅为格式示例，不能直接当作真实讲座发布：

```yaml
---
title: "讲座标题"
date: "2026-09-30" # 发布日期，不能晚于希望首次展示的日期
event_date: "2026-11-15T20:00:00+08:00" # 开始时间，必须包含时区
event_end: "2026-11-15T21:00:00+08:00" # 可选：结束时间，建议填写
speaker: "讲者姓名 · 单位"
summary: "一句话介绍讲座"
draft: true # 确认内容后改为 false
---

讲座摘要、讲者简介，以及已确认的参会链接。

[参加讲座](真实参会链接)
```

构建时按 `event_end`（未填则使用 `event_date`）自动分到 Upcoming 或 Past，预告按时间正序、往期按倒序排列。列表与详情默认显示 UTC 时间；可用 `display_time` 提供带明确时区的本地时间，例如 `29 September 2026 · 19:00–21:00 (UTC+8)`。**静态网站须重新构建发布后，活动才会从 Upcoming 移入 Past。** 在往期讲座正文添加回放、幻灯片链接即可。

## 本地预览

项目 `.Rprofile` 固定使用 Hugo **0.116.1 extended**。已有安装时运行：

```sh
hugo server --destination /tmp/omics4health-preview --baseURL http://localhost:1313
```

确保使用上述 Hugo 版本；RStudio/blogdown 会使用项目指定的版本。预览写入临时目录，避免将 localhost 地址发布到线上。

## GitHub 发布

- 源码仓库：`https://github.com/omics4health/omics4health-website`，分支 `main`。
- 网站仓库：`https://github.com/omics4health/omics4health.github.io`，分支 `main`；本地位于 `public/`，拥有独立的 Git 历史。
- 正式网址：`https://omics4health.github.io/`。

使用 Hugo 0.116.1 extended，以正式 baseURL 构建到一个干净的临时目录；验证页面和资源后，将产物同步到 `public/`，保留其中的 `.git/`。分别提交并推送网站产物和源码，并在源码提交中更新 `public` 的 Git 提交指针。不要提交本地预览、系统文件、同步缓存或无关文件权限变化。

## 第一期往期活动

资料保存在 `content/event/2026-09-29-qi-su/`。`poster.png` 和 `session.jpg` 为组织者提供的原始文件，摘要转录自海报。海报未单列时区，按香港及中国内地会议时间采用 UTC+8。可选字段 `title_zh`、`series`、`poster` 用于中文题目、期数和归档缩略图。

## 跨时区讲座时间

第二期为 `content/event/2026-11-04-zhi-luo-deng/index.md`。默认按 2026 年安排，起止时间为北京时间 11 月 4 日 20:00–21:00。论文标题与 DOI 经 PubMed 和 HZI 官网核对；活动标题暂采用论文题目，未补造正式摘要、主持人或会议链接。

`timezones` 中的 `zone` 使用 IANA 标识（Asia/Shanghai、Europe/Berlin、America/New_York）。`static/js/event-timezones.js` 根据 `event_date` 和 `event_end` 自动显示各地时间并处理夏令时；`fallback` 用于 JavaScript 不可用时的静态后备显示，修改日期时须同步更新。冬季与夏季换算均已验证。
