# 蒋奕达个人网站

这是一个使用 Quarto 构建的个人学术网站，展示我的研究方向和学术成果。

## 网站结构

- `index.qmd` - 首页，包含个人简介和研究方向
- `about.qmd` - 关于页面，详细的教育背景和技术技能
- `_quarto.yml` - 网站配置文件
- `styles.css` - 自定义样式文件

## 本地预览

1. 安装 Quarto：https://quarto.org/docs/get-started/
2. 在项目目录下运行：
   ```bash
   quarto preview
   ```
3. 打开浏览器访问 http://localhost:4200

## 部署到 GitHub Pages

1. 将代码推送到 GitHub 仓库
2. 在仓库设置中启用 GitHub Pages
3. 选择 "gh-pages" 分支作为发布源
4. 网站将自动部署到：https://[用户名].github.io/[仓库名]

## 技术栈

- **Quarto** - 文档发布系统
- **Markdown** - 内容编写
- **CSS** - 样式定制
- **GitHub Actions** - 自动部署

## 更新内容

编辑对应的 `.qmd` 文件后，提交更改到 GitHub，网站将自动更新。