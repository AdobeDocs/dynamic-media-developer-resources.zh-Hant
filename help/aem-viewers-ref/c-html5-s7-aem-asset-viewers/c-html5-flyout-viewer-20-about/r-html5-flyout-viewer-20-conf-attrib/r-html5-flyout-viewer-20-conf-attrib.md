---
title: 命令引用 — 配置屬性
description: Flyout Viewer的配置屬性文檔
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令引用 — 配置屬性{#command-reference-configuration-attributes}

Flyout Viewer的配置屬性文檔

可以在URL中設定任何配置命令。 或者，你可以 `setParam()`。 `setParams()`或兩個API方法。 也可以在伺服器端配置記錄中指定任何配置屬性。

某些配置命令的前置詞是相應Viewer SDK元件的類名或實例名。 元件的實例名稱是動態的，取決於傳遞給的查看器容器DOM元素的ID `setContainerId()` API方法。 文檔中包含此類命令的可選前置詞。 例如， `zoomfactor` 命令的說明如下：

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

命令的用法如下：

* `zoomfactor` （短語法）
* `FlyoutZoomView.zoomfactor` （用元件類名限定）
* `cont_flyout.zoomfactor` (使用元件ID限定，假定 `cont` 是容器元素的ID)

另請參閱 [所有查看器通用的命令引用 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
