---
title: 命令引用 — 配置屬性
description: Interactive Image Viewer的配置屬性文檔。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令引用 — 配置屬性{#command-reference-configuration-attributes}

Interactive Image Viewer的配置屬性文檔。

可以在URL中或使用 `setParam()`或 `setParams()`或兩者兼有的API方法。 也可以在伺服器端配置記錄中指定任何配置屬性。

某些配置命令可能以相應Viewer SDK元件的類名或實例名為前置詞。 元件的實例名稱是動態的，取決於傳遞給的查看器容器DOM元素的ID `setContainerId()` API方法。 文檔中包含此類命令的可選前置詞。 比如說， `zoomstep` 命令的說明如下：

`[ZoomView.|<containerId>_zoomView].fmt`

這意味著您可以將此命令用作：

* `fmt` （短語法）
* `ZoomView.fmt` （使用元件類名限定）
* `cont_zoomView.fmt` (使用元件ID限定，假定 `cont` 是容器元素的ID)

另請參閱 [所有查看器通用的命令引用 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
