---
description: 命令值必須使用%xx逸出序列進行http編碼，因此值字串不包含保留字元'='、'&'和'%'。
solution: Experience Manager
title: 影像轉換HTTP編碼
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# 影像轉換HTTP編碼{#image-rendering-http-encoding}

命令值必須使用%xx逸出序列進行http編碼，因此值字串不包含保留字元&#39;=&#39;、&#39;&amp;&#39;和&#39;%&#39;。

否則，會套用標準HTTP編碼規則。 HTTP規範要求對「（空格）」、「」（雙引號）、「#」、「%」、「&lt;」和「>」等不安全字元以及任何控制字元（如`<return>`和`<tab>`）進行編碼。

**注意：** 用作請求巢狀分隔字元的大括弧{ }不得進行編碼。某些電子郵件用戶端不幸地在內嵌的HTTP要求中編碼大括弧。 如果這是問題，「影像轉換」允許使用括弧()而非大括弧。

## 範例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上述請求片段必須編碼如下：

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 另請參閱 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1規範(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
