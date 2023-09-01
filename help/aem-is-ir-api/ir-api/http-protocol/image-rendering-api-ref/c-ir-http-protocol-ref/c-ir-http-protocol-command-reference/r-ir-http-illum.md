---
title: illum
description: 照明地圖選取器。 指定此材質偏好呈現的照明對映。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# illum{#illum}

照明地圖選取器。 指定此材質偏好呈現的照明對映。

`illum=-1|0|1|2`

如果目標暈映中沒有指定的照明對映，則會改用最近的可用對映。

`illum=-1` 指定根據下列條件自動選取照明對映 `gloss=` 值。

## 屬性 {#section-aace8466566e4cf1a0c5a6c0167245c9}

材質屬性。 如果暈映未定義多個照明對映，則忽略。

## 預設 {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## 另請參閱 {#section-9132e60381c64aa3a8ed1319690db55e}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
