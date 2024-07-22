---
description: 圖層會按照layer=指令指定的順序進行組合，其中編號較高的圖層會隱藏編號較低的圖層。
solution: Experience Manager
title: 合成畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# 合成畫布{#the-compositing-canvas}

圖層會按照layer=指令指定的順序進行組合，其中編號較高的圖層會隱藏編號較低的圖層。

圖層0構成背景圖層，背景圖層永遠是必要的，並定義複合影像的大小。 圖層0允許使用任何圖層型別。 必須根據內容影像或文字，明確使用`size=`或隱含地定義圖層0的大小。 其他圖層中落在圖層0區域之外的任何區域都不會包含在輸出影像中。

>[!NOTE]
>
>將所有圖層平面化之後，複合影像會轉換成最終回應影像，如[檢視命令和屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)所指定。
