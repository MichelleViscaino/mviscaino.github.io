---
layout: page
title: "Search"
permalink: /search/
---

<input id="search-input" type="text" placeholder="Search pages and teaching notes..." style="width:100%;padding:10px;font-size:16px;">
<ul id="results-container"></ul>

<script src="https://cdn.jsdelivr.net/npm/simple-jekyll-search@1.10.0/dest/simple-jekyll-search.min.js"></script>
<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: '{{ "/search.json" | relative_url }}',
    searchResultTemplate: '<li><a href="{url}">{title}</a></li>',
    noResultsText: '<li>No results found.</li>',
    limit: 20
  });
</script>