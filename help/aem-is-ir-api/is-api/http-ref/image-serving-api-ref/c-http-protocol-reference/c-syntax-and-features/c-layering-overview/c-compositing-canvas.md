---
description: 層按layer=命令指定的順序合成，其中編號較高的層隱藏編號較低的層。
solution: Experience Manager
title: 複合畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 複合畫布{#the-compositing-canvas}

層按layer=命令指定的順序合成，其中編號較高的層隱藏編號較低的層。

第0層構成背景層，該背景層始終是必需的，並定義複合影像的大小。 允許對層0使用任何層類型。 必鬚根據內容影像或文本，顯式使用`size=`或隱式定義層0的大小。 在輸出影像中，不包括位於層0區域之外的其它層的任何區域。

>[!NOTE]
>
>所有圖層平面化後，複合影像將轉換為最終響應影像，如[view命令和屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)所指定。
