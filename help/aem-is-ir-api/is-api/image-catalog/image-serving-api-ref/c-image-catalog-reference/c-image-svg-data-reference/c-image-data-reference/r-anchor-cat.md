---
description: 影像錨點。 將此影像用作模板或複合影像中的圖層時的原始點。
seo-description: 影像錨點。 將此影像用作模板或複合影像中的圖層時的原始點。
seo-title: 錨點
solution: Experience Manager
title: 錨點
topic: Scene7 Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# 錨點{#anchor}

影像錨點。 將此影像用作模板或複合影像中的圖層時的原始點。

也定義了旋轉的預設中心點。

## 屬性 {#section-95740f14160744e7bc763094b8be40d8}

兩個整數，以逗號分隔。 全解析度影像的左上角像素偏移。

覆寫 `anchor=`者(反過來可以用覆寫 `origin=`)。

## 預設 {#section-ca3a4cc837d643519eff15951f2b47a1}

如果此欄位不存在或為空白，且此為有效的影像記錄（即有效），則會使用影像的 `catalog::Path` 中心點。

## 另請參閱 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[錨點=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [原點=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
