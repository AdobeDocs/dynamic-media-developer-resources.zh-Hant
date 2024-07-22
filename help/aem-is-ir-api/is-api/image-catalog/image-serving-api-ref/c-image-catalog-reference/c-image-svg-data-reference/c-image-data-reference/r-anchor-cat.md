---
description: 影像錨點。 此影像在範本或複合影像中作為圖層使用時的原點。
solution: Experience Manager
title: 錨點
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# 錨點{#anchor}

影像錨點。 此影像在範本或複合影像中作為圖層使用時的原點。

也會定義預設的旋轉中心點。

## 屬性 {#section-95740f14160744e7bc763094b8be40d8}

兩個整數，以逗號分隔。 相對於全解析度影像左上角的畫素位移。

由`anchor=`覆寫（可由`origin=`覆寫）。

## 預設 {#section-ca3a4cc837d643519eff15951f2b47a1}

如果此欄位不存在或空白，而且這是有效的影像記錄（亦即`catalog::Path`有效），則會使用影像的中心點。

## 另請參閱 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ， [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
