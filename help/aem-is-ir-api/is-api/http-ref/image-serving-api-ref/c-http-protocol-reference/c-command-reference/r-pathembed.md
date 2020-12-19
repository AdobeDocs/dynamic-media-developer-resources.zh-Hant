---
description: 內嵌路徑資料。 指定是否應將圖層0來源影像檔案的Photoshop路徑包含在回應影像中。
seo-description: 內嵌路徑資料。 指定是否應將圖層0來源影像檔案的Photoshop路徑包含在回應影像中。
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: 93e63c7c-c091-4bb1-baff-45706fd611ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# pathEmbed{#pathembed}

內嵌路徑資料。 指定是否應將圖層0來源影像檔案的Photoshop路徑包含在回應影像中。

`pathEmbed=0|1`

## 屬性 {#section-26eb1c9e13574a0eae39f6d5b92c8995}

請求屬性。 如果源映像不包含路徑資料，則忽略。 路徑資料會像影像資料一樣縮放和旋轉。 僅處理`layer=0`源映像的路徑；會忽略其他圖層影像的路徑。

如果輸出影像格式不支援路徑內嵌，則會忽略。 有關支援路徑嵌入的輸出影像格式的清單，請參閱`fmt=`的說明。

## 限制{#section-697cddb79a1542bc8457d2f4f59eec69}

目前不支援將開放Photoshop路徑（不形成封閉回圈的路徑）內嵌至回應影像。

## 預設 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`，因為輸出影像中沒有內嵌路徑。

## 另請參閱 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
