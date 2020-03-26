---
description: 內嵌XMP中繼資料。 指定是否應將XMP中繼資料包含在回應影像中。
seo-description: 內嵌XMP中繼資料。 指定是否應將XMP中繼資料包含在回應影像中。
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# xmpEmbed{#xmpembed}

內嵌XMP中繼資料。 指定是否應將XMP中繼資料包含在回應影像中。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP資料從源影像傳遞到響應影像而不進行修改。 這可能導致錯誤資料嵌入到響應影像中。

## 屬性 {#section-27024c4272f44d9a8c264a0629193af2}

請求屬性。 如果來源影像未包含XMP資料，則會忽略。 僅處理來自源影像的XMP `layer=0` 資料。 其他圖層影像的XMP資料會被忽略。

如果輸出影像格式不支援XMP內嵌，則忽略此點。 有關支援XMP內嵌 `fmt=` 的輸出影像格式清單，請參閱的說明。

## 預設 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`，因為輸出影像中沒有內嵌路徑。

## 另請參閱 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
