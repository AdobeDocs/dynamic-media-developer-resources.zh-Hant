---
description: 影像錨點。 指定可重複紋理、壁框或貼花影像的錨點（熱點）。
solution: Experience Manager
title: 錨點
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
TQID: 'https://experienceleague.adobe.com/-TWQdh61Hkdr81vXooodDafEwQHTMvQdSQSf--HuPIg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 161
ht-degree: 3%

---

# 錨點{#anchor}

影像錨點。 指定可重複紋理、壁框或貼花影像的錨點（熱點）。

重複紋理會套用至暈映物件，使紋理錨點位於物件的紋理原點。 貼花影像會套用至暈映物件，使貼花錨點位於物件的貼花原點。 對於壁邊界，僅使用x值；會忽略y值。

## 屬性 {#section-bc4bc8b897c64535b88681e57d72942f}

兩個整數，以逗號分隔。 相對於影像左上角的畫素位移。 若`catalog::Alignment=3`和以純色及機櫃材料顯示，則忽略。

## 預設 {#section-b7ccc419a356415294706cd295ae96c9}

如果欄位空白或不存在，則會使用可重複紋理材質影像的左上角(0,0)，如果是貼花材質，則使用影像的中心。

## 另請參閱 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[目錄：：Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ， [錨點=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
