---
# Page title
#title: 《大数据存储技术》课程

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: 文献搜索


# Date page published
date: 2025-06-03

# Book page type (do not modify).
type: docs

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 1
---

  <p>若未打开搜索页面，请点击下方按钮：</p>
  <button id="openButton" class="btn" style="background-color: #4CAF50; color: white;">打开文献搜索页面</button>
  
  <script>
    // 用户点击后打开（最可靠）
    document.getElementById('openButton').addEventListener('click', function() {
      window.open('/search/so.html', '_blank');
    });
       // 可选：页面加载后延迟打开（可能被拦截）
    setTimeout(() => {
        window.open('/search/so.html', '_blank');    
    },1000); // 5秒后提示
  </script>