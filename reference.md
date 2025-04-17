---
layout: page
title: 参考资料
parent: 文档资料
nav_order: 2
permalink: /reference/
---

# 参考资料
{: .no_toc }

<details open markdown="block">
  <summary>
    目录
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

本页面提供各类技术规范、API文档和参考手册，帮助您快速查找所需信息。

## 技术规范

### 行业标准
{: .d-inline-block }

权威
{: .label .label-blue }

- [IEEE 754](https://en.wikipedia.org/wiki/IEEE_754) - 浮点数计算标准
- [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) - 日期和时间表示标准
- [Unicode 14.0](https://unicode.org/) - 字符编码标准

### 编程语言规范

常用编程语言的官方规范文档：

| 语言 | 版本 | 规范链接 | 备注 |
|:-----|:-----|:---------|:-----|
| Python | 3.10 | [Python 语言参考](https://docs.python.org/3/reference/index.html) | 包含语法和语义 |
| JavaScript | ES2022 | [ECMAScript 规范](https://tc39.es/ecma262/) | ECMA-262 标准 |
| C++ | C++20 | [ISO/IEC 14882:2020](https://www.iso.org/standard/79358.html) | 需购买访问 |

## API 文档

### REST API 设计指南

学习设计符合最佳实践的REST API：

1. **资源命名**
   - 使用名词表示资源：`/users` 而非 `/getUsers`
   - 使用复数形式：`/articles` 而非 `/article`

2. **HTTP方法**
   - GET：获取资源
   - POST：创建资源
   - PUT：更新资源
   - DELETE：删除资源
   - PATCH：部分更新资源

### 示例API文档

```json
{
  "openapi": "3.0.0",
  "info": {
    "title": "示例API",
    "version": "1.0.0",
    "description": "这是一个示例API文档"
  },
  "paths": {
    "/users": {
      "get": {
        "summary": "获取用户列表",
        "responses": {
          "200": {
            "description": "成功",
            "content": {
              "application/json": {
                "schema": {
                  "type": "array",
                  "items": {
                    "type": "object",
                    "properties": {
                      "id": { "type": "integer" },
                      "name": { "type": "string" }
                    }
                  }
                }
              }
            }
          }
        }
      }
    }
  }
}
```

## 术语表

常用专业术语解释：

<dl>
  <dt>API</dt>
  <dd>应用程序接口(Application Programming Interface)，定义了不同软件组件之间的交互方式。</dd>
  
  <dt>REST</dt>
  <dd>表述性状态传递(Representational State Transfer)，一种软件架构风格，用于设计网络应用程序。</dd>
  
  <dt>JSON</dt>
  <dd>JavaScript对象表示法(JavaScript Object Notation)，一种轻量级的数据交换格式。</dd>
</dl>

## 常见问题解答

{: .important }
这些问题基于用户最常搜索的内容整理而成。如果您没有找到所需答案，请[联系我们](/about/#联系方式)。

<details>
  <summary>如何引用这些参考资料？</summary>
  
  您可以使用以下格式引用本站的参考资料：
  
  ```
  文档网站 (2025). 参考资料: [标题]. 获取自 https://example.com/reference/
  ```
</details>

<details>
  <summary>这些资料多久更新一次？</summary>
  
  我们会定期检查和更新参考资料，确保内容的准确性和时效性。大部分内容每季度更新一次，但对于重要的标准变更，我们会及时更新。
</details>

## 相关资源

- [教程](/tutorials) - 与这些参考资料相关的教程
- [文档下载](/documents) - 可下载的完整文档

# 配置参考

以下为常用配置选项：

## 主题与外观
- `remote_theme`: 主题仓库
- `color_scheme`: 颜色方案 (`light`, `dark`, `custom`)
- `heading_anchors`: 是否启用标题锚点

## 导航与侧边栏
- `nav_sort`: 排序规则 (`case_sensitive`, `case_insensitive`)
- `collapse_title`: 侧边栏收起文本
- `aux_links`: 辅助导航链接

## 功能增强
- `search_enabled`: 启用搜索
- `enable_copy_code_button`: 代码复制按钮
- `mermaid.version` / `mermaid.config`: Mermaid 图表支持

更多配置项请参阅：https://just-the-docs.github.io/just-the-docs/docs/configuration/