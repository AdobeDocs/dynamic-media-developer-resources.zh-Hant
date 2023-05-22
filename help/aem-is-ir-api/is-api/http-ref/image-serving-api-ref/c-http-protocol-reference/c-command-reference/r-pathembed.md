---
description: 嵌入路徑資料。 指定是否應將來自第0層源映像檔案的Photoshop路徑包含在響應映像中。
solution: Experience Manager
title: 路徑嵌入
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# 路徑嵌入{#pathembed}

嵌入路徑資料。 指定是否應將來自第0層源映像檔案的Photoshop路徑包含在響應映像中。

`pathEmbed=0|1`

## 屬性 {#section-26eb1c9e13574a0eae39f6d5b92c8995}

請求屬性。 如果源映像不包含路徑資料，則忽略。 路徑資料被像影像資料一樣縮放和旋轉。 僅源映像的路徑 `layer=0` 處理；忽略來自其他圖層影像的路徑。

如果輸出影像格式不支援路徑嵌入，則忽略。 請參閱 `fmt=` 的子菜單。

## 限制 {#section-697cddb79a1542bc8457d2f4f59eec69}

此時不支援將開放Photoshop路徑（不形成封閉環的路徑）嵌入到響應影像中。

## 預設 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`，以在輸出影像中不嵌入路徑。

## 另請參閱 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
