---
description: 層按layer=命令指定的順序合成，其中編號較高的層隱藏編號較低的層。
solution: Experience Manager
title: 合成畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# 合成畫布{#the-compositing-canvas}

層按layer=命令指定的順序合成，其中編號較高的層隱藏編號較低的層。

第0層構成背景層，它始終是必需的，並定義了複合影像的大小。 層0允許使用任何層類型。 必須定義層0的大小，或者顯式使用 `size=` 或隱式。 輸出影像中不包括位於層0區域之外的其它層的任何區域。

>[!NOTE]
>
>將所有圖層拼合後，複合影像將轉換為最終響應影像，如 [查看命令和屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)。
