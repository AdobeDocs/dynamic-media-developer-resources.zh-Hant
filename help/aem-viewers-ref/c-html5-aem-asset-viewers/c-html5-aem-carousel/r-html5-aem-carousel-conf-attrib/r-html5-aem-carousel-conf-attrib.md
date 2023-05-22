---
title: 命令引用 — 配置屬性
description: Carousel Viewer的配置屬性文檔。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 71c2c973-d711-4d37-b778-381a7ec71527
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 命令引用 — 配置屬性{#command-reference-configuration-attributes}

Carousel Viewer的配置屬性文檔。

可以在URL中或使用 `setParam()`或 `setParams()`或兩者兼有的API方法。 也可以在伺服器端配置記錄中指定任何配置屬性。

某些配置命令可能以相應Viewer SDK元件的類名或實例名為前置詞。 元件的實例名稱是動態的，取決於傳遞給的查看器容器DOM元素的ID `setContainerId()` API方法。 文檔中包含此類命令的可選前置詞。 比如說， `zoomstep` 命令的說明如下：

`[ZoomView.|<containerId>_carouselView].fmt`

在這種情況下，您可以使用以下命令：

* `fmt` （短語法）
* `CarouselView.fmt` （使用元件類名限定）
* `cont_carouselView.fmt` (使用元件ID限定，假定 `cont` 是容器元素的ID)

另請參閱 [所有查看器通用的命令引用 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
