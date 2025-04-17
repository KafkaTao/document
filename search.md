---
layout: page
title: Search
description: "搜索网站内容"
permalink: /search/
nav_order: 10
---

# 搜索

Just the Docs 内置站内搜索功能。

- 启用搜索：`search_enabled: true`
- 自定义搜索显示层级：`search.heading_level`
- 预览文字数：`search.previews`
- 关键字分隔符：`search.tokenizer_separator`

更多细节请参考官方文档的 Search 章节。

{: .no_toc }

<div class="search">
  <div class="search-input-wrap">
    <input type="text" id="search-input" class="search-input" tabindex="0" placeholder="输入搜索关键词..." aria-label="搜索" autocomplete="off">
    <label for="search-input" class="search-label"><svg viewBox="0 0 24 24" class="search-icon"><use xlink:href="#svg-search"></use></svg></label>
  </div>
  <div id="search-results" class="search-results"></div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  // 等待Just the Docs的搜索功能加载
  setTimeout(function() {
    const searchInput = document.getElementById('search-input');
    if(searchInput) {
      // 从URL参数中获取查询
      const urlParams = new URLSearchParams(window.location.search);
      const query = urlParams.get('q');
      
      // 如果有查询参数，自动填充搜索框并触发搜索
      if(query) {
        searchInput.value = query;
        searchInput.dispatchEvent(new Event('input', { bubbles: true }));
      }
      
      // 聚焦搜索框
      searchInput.focus();
    }
  }, 500);
});
</script>