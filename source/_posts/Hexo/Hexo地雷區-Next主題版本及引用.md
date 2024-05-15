---
title: Hexo踩地雷 (1) | Next已經出到8了嗎
tags: 
- Hexo 
- Next 
- Next8
- 地雷
- 部落格
categories: Hexo
keywords: Next,
abbrlink: 2910137742
description: 網路上最容易搜尋到的資源非Hexo莫屬，o中文資源也較豐富，NexT主題也多數人選擇的主題之一。然而資源雖多，卻因為Hexo及NexT版本迭代速度較快，導致有些資源並不適用於現今的版本。因此本系列文，將會講述在新版的使用以及避雷方式。
date: 2024-04-15 04:38:00

---
## 前言
撰寫部落格應該是最能證明自己曾經付出過哪些努力的證據。那麼說到架設部落格，網路上最容易搜尋到的資源非Hexo莫屬，作為華人工程師的驕傲，Hexo中文資源也較豐富，此外 NexT 主題也是Hexo多數人選擇的主題之一。
<!-- More -->
然而資源雖多，卻因為Hexo及Nest版本迭代速度較快，導致有些資源並不適用於現今的版本。這就造成在架設時容易踩到一些地雷。
因此本系列文，將會講述為何版本迭代速度如此之快，以及在新版的使用以及避雷方式。

<!-- 另外，筆者推薦各位可以先閱讀這篇文章，Ray(israynotarray)大大的{% link 「試著學Hexo」 https://israynotarray.com/tags/%E8%A9%A6%E8%91%97%E5%AD%B8-Hexo/  [試著學Hexo] %} 系列文章，雖然該系列文版本不是目前最新的(Hexo4+Nest7)，但還是相當受用。如果真的踩到雷，我接下來的這幾篇文，應該對你有幫助! -->
<br>

## What is Hexo ?

一切的起因得從作者 tommy351 的這篇文章開始=> {% link Hexo 颯爽登場！ https://zespia.me/blog/2012/10/11/hexo-debut/  [Hexo 颯爽登場！] %}。
2012年的時候作者對於時下部落格框架( {% link jekyll https://github.com/jekyll/jekyll  [jekyll官網] %}、{% link octopress http://octopress.org/  [octopress官網] %} ) 的編譯器都有其缺點，編譯速度太慢、原開發者更新速度緩慢、學習成本過高等緣故，因此決定自己造輪子才有了現在的 {% link Hexo  https://hexo.io/zh-tw/index.html  [Hexo官網] %}。

Hexo不僅解決了當時作者提到的一些問題，現今發展至今已經到 Hexo7 了，國內外有不少開發者，在支撐這個框架的發展，此外由於是作者的背景緣故，台灣及中國有相當大量的用戶，累積了不少中文文件，以至於對中文語系的開發者入手難度大幅降低。
<br>

## 安裝 Hexo cli
接下來，教大家如何安裝 Hexo cli。
其實Hexo的版本在安裝上沒什麼變，但在安裝前需要先確認，目前本機端的node.js的版本。
{% img [class names] https://res.cloudinary.com/dnu5rgtxl/image/upload/c_scale,w_500/normal-evan/ojchpfs9t0mqfvsyljlp.jpg '"Hexo7
需搭配node.js 14.0以上版本，(圖為 hexo cli 適合的 Node.js版本) " "hexo cli version"' %}

確認沒問題後，接著便可以複製下面的程式碼到終端機

{% codeblock  %}
npm install -g hexo-cli
{% endcodeblock %}

安裝完成後，可以輸入  __hexo -version__
如果有跑出下方的圖片的內容就算成功摟 !
{% img [class names] https://res.cloudinary.com/dnu5rgtxl/image/upload/v1713649356/normal-evan/zdxmbkvt3m3ibp5jljau.webp '"hexo 安裝成功" "hexo 安裝成功"' %}
<br>

## 建立部落格檔案

接著我們來建立部落格檔案
在終端機輸入

{% codeblock  %}
hexo init <檔案名稱>
{% endcodeblock %}

舉例:我要把檔案名稱取為 my-blog，就在上面輸入 hexo init my-blog
成功便會如同下圖，如果失敗請檢查自己的安裝路徑或是node.js有沒有正確安裝!
{% img [class names] https://res.cloudinary.com/dnu5rgtxl/image/upload/v1713650297/normal-evan/vo61kmaxypp65hgmdcwh.webp '"blog 建立成功訊息" "blog 建立成功訊息"' %}

接著在終端機中輸入這段程式碼進入資料夾，或是直接在資料中開啟VS code。
備註:請把檔案名稱的地方替換成自己的檔案名稱
{% codeblock  %}
cd <檔案名稱>
{% endcodeblock %}

接著再安裝node_modules，在終端機中輸入
{% codeblock  %}
npm install
{% endcodeblock %}
這邊會安裝比較久，不過安裝完就可以運行摟!
安裝完成會顯示如下圖~
{% img [class names] https://res.cloudinary.com/dnu5rgtxl/image/upload/v1713650792/normal-evan/jxkbi0ro8b1nqt3got14.webp '"node_modules安裝完成" "node_modules安裝完成"' %}
<br>

## 出來吧!我的部落格!

接著我們用VScode打開部落格資料夾，便會看到下圖的內容。
{% img [class names] https://res.cloudinary.com/dnu5rgtxl/image/upload/v1713652902/normal-evan/bzqc3scowjzthyawxgqq.webp '"hexo資料夾結構" "hexo資料夾結構"' %}

接著我們再終端機輸入
{% codeblock  %}
hexo s
{% endcodeblock %}

出現下圖的內容就表示本地伺服器開起來摟!
只要按著 `control` + 滑鼠點擊 `http://localhost:4000/`的位置(網址尾數不一定相同)
{% img [class names] https://res.cloudinary.com/dnu5rgtxl/image/upload/v1713653053/normal-evan/uaz78zrz4f4emjj2lmkn.webp '"hexo s" "hexo s"' %}

{% img [class names] https://res.cloudinary.com/dnu5rgtxl/image/upload/v1713653312/normal-evan/qe0hq5b4rcp9j36ccje7.webp '"部落格正式開啟" "部落格正式開啟"' %}
<br>

## FATAL: 4000 has been use
注意 如果按下`hexo s`卻出現如下圖，代表原本hexo 部署本地端伺服器的端口"4000"被佔用了。
{% img [class names] https://res.cloudinary.com/dnu5rgtxl/image/upload/v1713653441/normal-evan/fcyqoranbfnmmbx2cofx.webp
 '"port 4000 被佔用了" "port 4000 被佔用了"' %}

這個解決辦法也很簡單，只要把VScode關乾淨再打開就搞定了。
但如果該端口真的沒辦法關，也有解決辦法!
請在_config.yml中，在最後一行輸入下面的程式碼
{% codeblock yml %}
server:
  port: <任意數字不要跟現有本地端衝突即可>
  compress: true
  header: true
{% endcodeblock %}

圖例:
{% img [class names] https://res.cloudinary.com/dnu5rgtxl/image/upload/v1713654062/normal-evan/l1myfjzzyxfytnyalupl.webp
 '"port改為4001，解決問題! " "port改為4001，解決問題!"' %}

<br>
下一篇開始會開始講述 NexT主題的部分，也是雷最多的地方，準備好踩地雷了嗎!

<!-- ## Nest 主題
## What is Nest
從這邊開始雷點就出現了 -->

<!-- 
其實也不只Hexo，Hexo Nest主題其實才是改變最多的地方。

至於為什麼會改動很多，不全然是因為版本迭代，而是因為開發團隊經歷過"兩次"Github庫無人維護的狀況!
簡單來說就是權限所有人不再維護，又沒有把權限移交出去，導致開發團隊搬到新的repo。而這樣的事情總共經歷過兩次，並且各版本間在調整樣式的方式不太一樣，這也造成使用者在更新或者新使用者在架設時容易踩到雷的一個主因。

以筆者我來說，東西都安裝下去了才發現已經到V8了，只能重新來過(茶

也因此這邊文章會著重於2024年現今的版本撰寫，希望能幫助到一些要用新版本架設的新手們~~(不過前提是這篇文章要先被Google演算法眷顧)~~ -->