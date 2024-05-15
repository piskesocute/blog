---
title: "404 - 真巧，竟然在這裡遇到你！"
date: 2020-09-12 23:01:35
comments: false
permalink: /404.html
---

<!-- markdownlint-disable MD039 MD033 -->

## OOPS! 你跑錯地方摟，這是一個不存在的頁面!

{% img [class names] https://firebasestorage.googleapis.com/v0/b/blog-5da80.appspot.com/o/404%2F404.webp?alt=media&token=2c4b17ab-b514-406c-85a4-ff40fdc9e6f9 300 '"這是404 請轉身離開" "這是404 請轉身離開"' %}

很抱歉，你目前存取的頁面並不存在。

預計將在約 <span id="timeout">5</span> 秒後返回首頁。

如果你很急著想看文章，你可以 **[點這裡](https://normal-evan.com/)** 返回首頁。

<script>
let countTime = 5;

function count() {
  
  document.getElementById('timeout').textContent = countTime;
  countTime -= 1;
  if(countTime === 0){
    location.href = 'https://normal-evan.com/'; // 記得改成自己網址 Url
  }
  setTimeout(() => {
    count();
  }, 1000);
}

count();
</script>
