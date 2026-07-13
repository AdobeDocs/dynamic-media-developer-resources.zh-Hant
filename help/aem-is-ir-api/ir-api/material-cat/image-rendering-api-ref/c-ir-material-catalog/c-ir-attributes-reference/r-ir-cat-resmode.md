---
title: 解析模式
description: 重新取樣模式。 resMode=的預設值。 指定用來將演算後的影像縮放至最終大小的重新取樣和插值屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c57932a0-529c-4f31-b60e-a38de6fe277f
TQID: 'https://experienceleague.adobe.com/FZ76OaQf5qTWEDjwaLQ38GcgXsSnemM8xST9CmH9HPs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 4%

---

# 解析模式{#resmode}

重新取樣模式。 `resMode=`的預設。 指定用來將演算後的影像縮放至最終大小的重新取樣和插值屬性。

## 屬性 {#section-1183a155f33c4eca80f1dc6fb6bda1b5}

列舉。 設定`'bilin'`為2，`'bicub'`為3，或`'sharp2'`內插模式為4 （詳情請參閱[resMode=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md)）。

## 預設 {#section-ed432a0acc3e4bce926a07e9cfd2c865}

如果未定義或空白，則繼承自`default::ResMode`。

## 另請參閱 {#section-34b71c295b4349dfb4379823a2de83c2}

[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)

