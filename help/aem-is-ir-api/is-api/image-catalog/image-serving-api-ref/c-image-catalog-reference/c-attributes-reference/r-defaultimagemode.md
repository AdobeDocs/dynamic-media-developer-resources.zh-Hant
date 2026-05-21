---
description: 預設影像模式。 選取當找不到請求中指定的影像時如何套用預設影像。
solution: Experience Manager
title: 預設影像模式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
TQID: 'https://experienceleague.adobe.com/pe73D8ZWHMpPQSfd6KEk7rh4hD-eJCBuUrHC9n-yIUw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 2%

---

# 預設影像模式{#defaultimagemode}

預設影像模式。 選取當找不到請求中指定的影像時如何套用預設影像。

## 屬性 {#section-7fa8acb63540490d9f5186231b5e77c3}

列舉。 「0」會取代整個複合影像，即使遺失的影像隻是數個圖層之一；「1」會以預設影像取代每個遺失的圖層來源影像，並照常傳回複合影像。

## 限制 {#section-04cb0d50e8914564a8d226d0d4663c8b}

巢狀影像轉譯、FXG或`req=set`要求失敗時，「影像伺服」會回覆為`DefaultImageMode=0`。

## 預設 {#section-9e318524a2a5496386901286748c7ee7}

如果未定義或空白，則繼承自`default::DefaultImage`。

## 另請參閱 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ， [attribute：：DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
