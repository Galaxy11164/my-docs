# my-docs

开源软件设计与分析课程 实验二 第二部分：用 GitHub Actions 构建 MkDocs 静态站点并部署到 GitHub Pages。

## 目录结构

```
my-docs/
├── docs/                          # Markdown 文档源文件
│   ├── index.md                   # 主页
│   ├── about.md                   # 关于页面
│   ├── guide.md                   # 使用指南
│   └── api.md                     # API 参考
├── .github/workflows/deploy.yml   # 自动化部署工作流
├── mkdocs.yml                     # MkDocs 配置文件
└── README.md
```

## 本地预览

```bash
pip install mkdocs-material
mkdocs serve      # http://127.0.0.1:8000
```

## 部署

向 `main` 分支推送 `docs/**` 或 `mkdocs.yml` 的改动后，Actions 会自动构建并推送到
`gh-pages` 分支，站点地址为 `https://<用户名>.github.io/my-docs/`。