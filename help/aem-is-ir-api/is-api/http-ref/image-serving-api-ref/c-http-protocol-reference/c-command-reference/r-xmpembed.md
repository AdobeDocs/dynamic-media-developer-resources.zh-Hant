---
description: 內嵌中XMP繼資料。 指定回XMP應影像中是否應包含中繼資料。
seo-description: 內嵌中XMP繼資料。 指定回XMP應影像中是否應包含中繼資料。
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---


# xmpEmbed{#xmpembed}

內嵌中XMP繼資料。 指定回XMP應影像中是否應包含中繼資料。

`xmpEmbed=0|1`

>[!NOTE]
>
>資料XMP從源影像傳遞到響應影像而不進行修改。 這可能導致錯誤資料嵌入到響應影像中。

## 屬性 {#section-27024c4272f44d9a8c264a0629193af2}

請求屬性。 如果源映像不包含資料，則忽略XMP此選項。 僅XMP處理來自`layer=0`源映像的資料。 其XMP他圖層影像的資料會被忽略。

如果輸出影像格式不支援內嵌，則會忽略XMP此點。 有關支援嵌入的輸出影像格式清單，請參閱`fmt=`的說XMP明。

## 預設 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`，因為輸出影像中沒有內嵌路徑。

## 另請參閱 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
