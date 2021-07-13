---
description: 預設視圖大小。
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 709fb2a1-1b9d-421e-9a65-5f5c74390ce3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 4%

---

# DefaultPix{#defaultpix}

預設視圖大小。

如果請求未使用`wid=`、`hei=`或`scl=`明確指定檢視大小，則伺服器會限制回覆影像不大於此寬度和高度。

## 屬性 {#section-c3e658cf82c540d986b118f74f0fe1b2}

兩個整數，0或更大，以逗號分隔。 寬度和高度（像素）。 可將任一或兩個值設為0，以保持它們不受約束。

不適用於巢狀/內嵌的請求。

## 預設 {#section-b7338b2bf5114fff83b0714a57b20639}

如果未定義或為空，則從`default::DefaultPix`繼承。

## 另請參閱 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), scl= [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [ catalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
