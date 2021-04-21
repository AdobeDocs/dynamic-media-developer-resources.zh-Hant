---
description: Flyout Viewer的設定屬性檔案
solution: Experience Manager
title: 命令參考——配置屬性
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# 命令參考——配置屬性{#command-reference-configuration-attributes}

Flyout Viewer的設定屬性檔案

您可以在URL中設定任何組態命令。 或者，您可以使用`setParam()`、`setParams()`或兩種API方法。 您也可以在伺服器端組態記錄中指定任何組態屬性。

某些組態命令會加上類別名稱或對應Viewer SDK元件的例項名稱前置詞。 元件的例項名稱是動態的，並視傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID而定。 說明檔案包含此類命令的可選首碼。 例如，`zoomfactor`命令的說明如下：

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

命令的用法如下：

* `zoomfactor` （簡短語法）
* `FlyoutZoomView.zoomfactor` （限定元件類名）
* `cont_flyout.zoomfactor` (以元件ID為限，假設 `cont` 是容器元素的ID)

另請參閱[所有查看器通用的命令參考——配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
