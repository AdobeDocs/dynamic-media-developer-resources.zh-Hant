---
title: 影像呈現HTTP編碼
description: 命令值必須使用%xx轉義序列進行http編碼，這樣值字串就不包括保留的字元「=」、「&」和「%」。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# 影像呈現HTTP編碼{#image-rendering-http-encoding}

命令值必須使用%xx轉義序列進行http編碼，這樣值字串就不包括保留的字元「=」、「&amp;」和「%」。

否則，將應用標準HTTP編碼規則。 HTTP規範要求對「 」（空格）、 「 」（雙引號）、 「# 」、 「 % 」、 「 &lt; 」和「> 」等不安全字元以及任何控制字元(如 `<return>` 和 `<tab>`。

**注意：** 不能對用作請求嵌套分隔符的大括弧{ }進行編碼。 某些電子郵件客戶端很遺憾地將嵌入的HTTP請求中的花括弧編碼。 如果此問題是問題，「影像呈現」允許使用圓括弧()而不是大括弧。

## 範例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上述請求片段必須按如下方式編碼：

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 另請參閱 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1規範(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
