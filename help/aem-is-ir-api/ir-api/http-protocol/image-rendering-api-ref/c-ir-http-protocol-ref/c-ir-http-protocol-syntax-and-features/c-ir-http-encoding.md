---
description: 命令值必須使用%xx轉義序列進行http編碼，這樣值字串就不包括保留字元「=」、「&」和「%」。
solution: Experience Manager
title: 影像呈現HTTP編碼
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# 影像呈現HTTP編碼{#image-rendering-http-encoding}

命令值必須使用%xx轉義序列進行http編碼，這樣值字串就不包括保留字元「=」、「&amp;」和「%」。

否則，會套用標準HTTP編碼規則。 HTTP規範要求對「（空格）」、「」（雙引號）、「#」、「%」、「&lt;」和「>」等不安全字元以及諸如`<return>`和`<tab>`等任何控制字元進行編碼。

**注意：** 用作請求巢狀分隔字元的大括弧{ }不得編碼。某些電子郵件用戶端不幸將大括弧編碼在內嵌HTTP要求中。 如果這是問題，影像轉譯允許使用括弧()而非大括弧。

## 範例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上述要求片段必須依下列方式編碼：

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 另請參閱 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1規範(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
