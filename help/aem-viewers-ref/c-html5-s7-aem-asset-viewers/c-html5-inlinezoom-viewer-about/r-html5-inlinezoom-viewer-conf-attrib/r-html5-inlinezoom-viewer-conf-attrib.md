---
title: 命令參考 — 組態屬性
description: 彈出式檢視器的設定屬性檔案
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

彈出式檢視器的設定屬性檔案

您可以在URL中設定任何組態命令。 或者，您可以使用`setParam()`、`setParams()`或兩者API方法。 您也可以在伺服器端組態記錄中指定任何組態屬性。

有些設定命令會加上相對應檢視器SDK元件的類別名稱或例項名稱作為前置詞。 元件的執行個體名稱是動態的，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素的識別碼。 檔案包含這類命令的選用首碼。 例如，`zoomfactor`命令的記錄如下：

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

命令的使用方式如下：

* `zoomfactor` （簡短語法）
* `FlyoutZoomView.zoomfactor` （以元件類別名稱限定）
* `cont_flyout.zoomfactor` （以元件ID限定，假設`cont`是容器元素的識別碼）

另請參閱所有檢視者通用的[命令參考 — 組態屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
