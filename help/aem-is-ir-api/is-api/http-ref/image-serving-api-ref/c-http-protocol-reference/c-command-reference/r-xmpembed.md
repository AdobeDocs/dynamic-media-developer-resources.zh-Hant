---
description: 嵌入元XMP資料。 指定XMP是否應將元資料包括在響應映像中。
solution: Experience Manager
title: xmp嵌入
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# xmp嵌入{#xmpembed}

嵌入元XMP資料。 指定XMP是否應將元資料包括在響應映像中。

`xmpEmbed=0|1`

>[!NOTE]
>
>數XMP據從源影像傳遞到響應影像而不進行修改。 這可能導致錯誤資料被嵌入到響應影像中。

## 屬性 {#section-27024c4272f44d9a8c264a0629193af2}

請求屬性。 如果源映像不包含資料，則忽XMP略。 僅來XMP自源映像的資料 `layer=0` 。 忽略XMP來自其他圖層影像的資料。

如果輸出影像格式不支援嵌入，則忽XMP略。 請參閱 `fmt=` 的子菜單。

## 預設 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`，以在輸出影像中不嵌入路徑。

## 另請參閱 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
