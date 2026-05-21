---
description: 圖層會按照layer=指令指定的順序進行組合，其中編號較高的圖層會隱藏編號較低的圖層。
solution: Experience Manager
title: 合成畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
TQID: 'https://experienceleague.adobe.com/WNvq6dLRetz3iEbtP0ugmOPagUfTCaa5eXdB3lEzEaQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 0%

---

# 合成畫布{#the-compositing-canvas}

圖層會按照layer=指令指定的順序進行組合，其中編號較高的圖層會隱藏編號較低的圖層。

圖層0構成背景圖層，背景圖層永遠是必要的，並定義複合影像的大小。 圖層0允許使用任何圖層型別。 必須根據內容影像或文字，明確使用`size=`或隱含地定義圖層0的大小。 其他圖層中落在圖層0區域之外的任何區域都不會包含在輸出影像中。

>[!NOTE]
>
>將所有圖層平面化之後，複合影像會轉換成最終回應影像，如[檢視命令和屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)所指定。
