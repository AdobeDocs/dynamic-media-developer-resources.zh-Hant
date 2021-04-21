---
description: 影像錨點。 將此影像用作模板或複合影像中的圖層時的原始點。
solution: Experience Manager
title: 錨點
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 5%

---


# 錨點{#anchor}

影像錨點。 將此影像用作模板或複合影像中的圖層時的原始點。

也定義了旋轉的預設中心點。

## 屬性 {#section-95740f14160744e7bc763094b8be40d8}

兩個整數，以逗號分隔。 全解析度影像的左上角像素偏移。

由`anchor=`覆寫（反過來可以由`origin=`覆寫）。

## 預設 {#section-ca3a4cc837d643519eff15951f2b47a1}

如果此欄位不存在或為空白，且此為有效的影像記錄（亦即，如果`catalog::Path`有效），則會使用影像的中心點。

## 另請參閱 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[錨點=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [原點=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
