---
description: 影像錨點。 將此影像用作模板或複合影像中的圖層時的原點。
solution: Experience Manager
title: 錨點
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# 錨點{#anchor}

影像錨點。 將此影像用作模板或複合影像中的圖層時的原點。

也定義旋轉的預設中心點。

## 屬性 {#section-95740f14160744e7bc763094b8be40d8}

兩個整數，用逗號分隔。 相對於全解析度影像的左上角的像素偏移。

由覆蓋 `anchor=`(這反過來又可以用 `origin=`)。

## 預設 {#section-ca3a4cc837d643519eff15951f2b47a1}

如果此欄位不存在或為空，並且這是有效的影像記錄(即，如果 `catalog::Path` 有效)。

## 另請參閱 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[錨=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) 。 [原產地=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
