---
description: eCatalog Viewer的配置屬性文檔。
solution: Experience Manager
title: 命令引用 — 配置屬性
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 命令引用 — 配置屬性{#command-reference-configuration-attributes}

eCatalog Viewer的配置屬性文檔。

可以在URL中或使用 `setParam()`或 `setParams()`或兩者兼有的API方法。 您還可以指定在伺服器端配置記錄中指定的任何配置屬性。

對於某些配置命令，可以使用相應Viewer SDK元件的類名或實例名為它們加上前置詞。 元件的實例名稱是動態的，取決於傳遞給的查看器容器DOM元素的ID `setContainerId()` API方法。 文檔包括此類命令的可選前置詞。 比如說， `zoomstep` 命令的說明如下：

`[PageView.|<containerId>_pageView].zoomstep`

這意味著您可以將此命令用作：

* `zoomstep` （短語法）
* `PageView.zoomstep` （使用元件類名限定）
* `cont_pageView.zoomstep` (使用元件ID限定，假定 `cont` 是容器元素的ID)

另請參閱 [所有查看器通用的命令引用 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
