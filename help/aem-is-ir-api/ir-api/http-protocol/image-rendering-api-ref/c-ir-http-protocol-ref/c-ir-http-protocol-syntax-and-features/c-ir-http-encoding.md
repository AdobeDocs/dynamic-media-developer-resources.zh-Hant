---
title: 影像演算HTTP編碼
description: 命令值必須使用%xx逸出序列進行http編碼，讓值字串不包含保留的字元'='、'&'和'%'。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# 影像演算HTTP編碼{#image-rendering-http-encoding}

命令值必須使用%xx逸出序列進行http編碼，讓值字串不包含保留的字元&#39;=&#39;、&#39;&amp;&#39;和&#39;%&#39;。

否則，將套用標準HTTP編碼規則。 HTTP規格需要對不安全的字元(例如&#39; &#39; （空格）、&#39;&#39;&#39; （雙引號）、&#39;#&#39;、&#39;%&#39;、&#39;&lt;&#39;和&#39;>&#39;)以及任何控制字元（例如`<return>`和`<tab>`）進行編碼。

**警告：**&#x200B;用作請求巢狀分隔符號的大括弧{ }不可編碼。 不幸的是，某些電子郵件使用者端會在內嵌HTTP請求中編碼大括弧。 如果這是問題所在，影像演算可允許使用括弧( )而非大括弧。

## 範例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上述請求片段必須編碼如下：

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 另請參閱 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1規格(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
