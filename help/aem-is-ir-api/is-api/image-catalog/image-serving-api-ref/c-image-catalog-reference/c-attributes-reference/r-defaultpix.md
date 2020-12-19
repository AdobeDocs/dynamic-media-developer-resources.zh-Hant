---
description: 預設檢視大小。
seo-description: 預設檢視大小。
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# DefaultPix{#defaultpix}

預設檢視大小。

如果請求未明確使用`wid=`、`hei=`或`scl=`指定檢視大小，則伺服器會限制回覆影像不大於此寬度和高度。

## 屬性 {#section-c3e658cf82c540d986b118f74f0fe1b2}

兩個整數，0或更大，以逗號分隔。 寬度和高度（以像素為單位）。 其中一個或兩個值都可設為0，以保持不受約束。

不適用於巢狀／內嵌請求。

## 預設 {#section-b7338b2bf5114fff83b0714a57b20639}

如果未定義或為空，則繼承自`default::DefaultPix`。

## 另請參閱 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [目錄：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
