---
title: 命令引用 — 配置屬性
description: Spin Viewer的配置屬性文檔。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 命令引用 — 配置屬性{#command-reference-configuration-attributes}

Spin Viewer的配置屬性文檔。

可以在URL中或使用 `setParam()`或 `setParams()`或兩者兼有的API方法。 也可以在伺服器端配置記錄中指定任何配置屬性。

某些配置命令可能以相應Viewer SDK元件的類名或實例名為前置詞。 元件的實例名稱是動態的，取決於傳遞給的查看器容器DOM元素的ID `setContainerId()` API方法。 文檔中包含此類命令的可選前置詞。 比如說， `zoomstep` 命令的說明如下：

`[SpinView.|<containerId>_spinView].zoomstep`

這意味著您可以按如下方式使用此命令

* `zoomstep` （短語法）
* `SpinView.zoomstep` （使用元件類名限定）
* `cont_spinView.zoomstep` (使用元件ID限定，假定 `cont` 是容器元素的ID)

另請參閱 [所有查看器通用的命令引用 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
