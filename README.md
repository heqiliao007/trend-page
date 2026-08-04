# GitHub Trending 实时解读

> 由 AI 自动抓取 GitHub Trending 仓库、阅读 README、撰写深度中文解读。

🌐 **页面地址：** https://heqiliao007.github.io/trend-page/

## 这是什么

这是一个自动更新的 GitHub Trending 展示页面。与传统 trending 页面不同，每个项目都配有**基于 README 实际内容**的中文深度解读——包括项目是做什么的、解决了什么问题、有什么亮点。

## 如何工作

| 步骤 | 说明 | 频率 |
|------|------|------|
| ① 抓取数据 | 通过 GitHub Search API 获取近一周有活跃推送的热门仓库 | 每 6 小时 |
| ② 读取 README | 逐一读取每个仓库的 README 获取项目全貌 | 有新仓库时 |
| ③ AI 深度解读 | Hermes Agent 用中文撰写项目解读 | 有新仓库时 |
| ④ 生成页面 | 构建 HTML 并推送到 GitHub Pages | 每 6 小时 |
| ⑤ 自动部署 | GitHub Pages 自动上线最新版本 | 推送后自动 |

## 技术栈

- **数据源：** GitHub Search API
- **AI 解读：** Hermes Agent（Nous Research）
- **托管：** GitHub Pages
- **自动化：** macOS crontab + Hermes cron

## 项目结构

```
├── index.html             # 页面文件（自动生成）
├── INSIGHTS_CACHE.json    # AI 解读缓存
└── README.md              # 本文件
```

## 相关链接

- 页面：https://heqiliao007.github.io/trend-page/
- 仓库：https://github.com/heqiliao007/trend-page
