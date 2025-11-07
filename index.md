---
layout: default
title: User Onboarding Service
description: Technical Specification Documentation
---

<link rel="stylesheet" href="/assets/style.css">

{% include_relative README.md %}

<!-- Mermaid support for rendering diagrams in fenced code blocks -->
<script src="https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.min.js"></script>
<script>
  mermaid.initialize({ startOnLoad: true, theme: 'neutral' });
  document.addEventListener('DOMContentLoaded', function () {
    // Convert fenced code blocks with language-mermaid into <div class="mermaid"> containers
    document.querySelectorAll('pre > code.language-mermaid').forEach(function (code) {
      var pre = code.parentElement;
      var container = document.createElement('div');
      container.className = 'mermaid';
      container.textContent = code.textContent;
      pre.parentElement.replaceChild(container, pre);
    });
  });
  // Optional: guard for older themes that wrap code differently
  document.addEventListener('DOMContentLoaded', function () {
    document.querySelectorAll('code.language-mermaid').forEach(function (code) {
      if (code.parentElement && code.parentElement.tagName.toLowerCase() !== 'pre') {
        var container = document.createElement('div');
        container.className = 'mermaid';
        container.textContent = code.textContent;
        code.parentElement.replaceChild(container, code);
      }
    });
  });
</script>