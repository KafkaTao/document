---
title: Blog
---
# 博客

欢迎阅读博客，关注以下分类：

- [技术文章](blog-tech.html)

---
layout: page
title: 博客
nav_order: 4
has_children: true
permalink: /blog/
---

# 博客文章

这里是我们发布的所有博客文章，包括技术分享、学习心得和行业动态等。

## 最新文章

{% assign sorted_posts = site.html_pages | where_exp: "item", "item.parent == 'blog'" | sort: "date" | reverse %}

<ul class="post-list">
{% for post in sorted_posts limit:5 %}
  <li>
    <span class="post-meta">{{ post.date | default: "2025-04-16" }}</span>
    <h3>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h3>
    {% if post.description %}
    <p>{{ post.description }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>

## 文章分类

- [技术教程](/blog/tech/) - 实用技术和开发指南
- [学习笔记](/blog/study/) - 学习过程中的心得体会
- [行业动态](/blog/news/) - 最新行业新闻与趋势分析