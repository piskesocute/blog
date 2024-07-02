---
title: ザ・ワールド！時よ止まれ！ 停止吧! 全部setInterval !!
abbrlink: 2438484395
date: 2024-07-03 02:44:19
tags: ['JavaScript', 'setInterval', 'setTimeout', 'clearInterval', '感謝來自前同事的地雷', ]
categories: JavaScript 的惡魯莫團
---

對於 setInterval ，我想大家在初學時期應該也都用過了，大致的功能也都知道了。簡單說明，在 JavaScript 中要操作時間或是利用時間間隔來實作定時器以觸發某些功能或函式，大部分人首先想到的應該就是 `setInterval` 以及 `setTimeout`，此外如果要停止 `setTimeout` 則要使用 `clearInterval`。

但大家知道，為什麼使用 `clearInterval` 要先幫 `setInterval` 先告一個變數嘛?
而這個變數裡頭到底存了什麼? 是 `Function`? `Object`?

接下來的內文便會介紹 `setInterval` 、 `clearInterval` 以及標題中提到的 `ZAWARUDO setInerval`

## setInterval() VS  setTimeout()

首先來介紹一下什麼是 `setTimeout()`