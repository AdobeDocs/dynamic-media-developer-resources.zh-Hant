---
description: 預設縮圖大小。 用於縮圖請求(req=tmb)，而非屬性DefaultPix。
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# DefaultThumbPix{#defaultthumbpix}

預設縮圖大小。 用於縮圖請求(req=tmb)，而非屬性：:DefaultPix。

如果縮圖要求(`req=tmb`)未明確指定大小，而未明確使用`wid=`、`hei=`或`scl=`指定檢視大小，伺服器會限制回覆影像不大於此寬度和高度。

## 屬性 {#section-650d9b1194fb4c47a03c6809e6b4af0e}

兩個整數，0或更大，以逗號分隔。 寬度和高度（以像素為單位）。 其中一個或兩個值都可設為0，以保持不受約束。

不適用於巢狀／內嵌請求。

## 預設 {#section-2c4a4f14540449638822913513170ff1}

如果未定義或為空，則繼承自`default::DefaultThumbPix`。

## 另請參閱 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
