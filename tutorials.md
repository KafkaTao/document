---
title: Tutorials
---
# 教程

本节介绍如何使用 Just the Docs 快速建立和定制你的文档站点。

## 1. 安装 Jekyll 和主题

```bash
gem install bundler jekyll
bundle add just-the-docs
```

## 2. 使用模板创建新站点

```bash
git clone https://github.com/just-the-docs/template.git my-site
cd my-site
bundle install
bundle exec jekyll serve --livereload
```

## 3. 配置站点

在 `_config.yml` 中添加或修改配置，示例：

```yaml
remote_theme: just-the-docs/just-the-docs
search_enabled: true
```