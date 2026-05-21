---
title: pathEmbed
description: 內嵌路徑資料。 指定回應影像中是否應包含來自0層來源影像檔案的Photoshop路徑。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
TQID: 'https://experienceleague.adobe.com/ES7nAoYjO6Y4naU2c5TIPotPUTjncwjRMLL7-4--XpE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 2%

---

# pathEmbed{#pathembed}

內嵌路徑資料。 指定回應影像中是否應包含來自0層來源影像檔案的Photoshop路徑。

`pathEmbed=0|1`

## 屬性 {#section-26eb1c9e13574a0eae39f6d5b92c8995}

要求屬性。 如果來源影像不包含路徑資料，則忽略。 路徑資料會像影像資料一樣縮放和旋轉。 僅處理`layer=0`來源影像的路徑；忽略其他圖層影像的路徑。

如果輸出影像格式不支援路徑內嵌，則忽略。 如需支援路徑內嵌的輸出影像格式清單，請參閱`fmt=`的說明。

## 限制 {#section-697cddb79a1542bc8457d2f4f59eec69}

目前不支援將開放Photoshop路徑（不構成封閉回圈的路徑）內嵌至回應影像。

## 預設 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`，輸出影像中不內嵌路徑。

## 另請參閱 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
