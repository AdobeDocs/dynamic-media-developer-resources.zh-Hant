---
title: 命令參考 — 組態屬性
description: 轉盤檢視器的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 71c2c973-d711-4d37-b778-381a7ec71527
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

轉盤檢視器的設定屬性檔案。

任何設定命令都可以在URL中設定，或使用`setParam()`、`setParams()`或兩者的API方法設定。 任何設定屬性也可在伺服器端設定記錄中指定。

某些設定命令可能會加上相對應檢視器SDK元件的類別名稱或例項名稱當作前置詞。 元件的執行個體名稱是動態的，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素的識別碼。 檔案包含這類命令的選用首碼。 例如，`zoomstep`命令的記錄如下：

`[ZoomView.|<containerId>_carouselView].fmt`

在這種情況下，您可以使用此命令：

* `fmt` （簡短語法）
* `CarouselView.fmt` （以元件類別名稱限定）
* `cont_carouselView.fmt` （以元件ID限定，假設`cont`是容器元素的識別碼）

另請參閱所有檢視者通用的[命令參考 — 組態屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
