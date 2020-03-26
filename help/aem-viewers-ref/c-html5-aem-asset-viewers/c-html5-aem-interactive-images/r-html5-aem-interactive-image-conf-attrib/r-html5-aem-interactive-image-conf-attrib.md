---
description: 互動式影像檢視器的設定屬性檔案。
seo-description: 互動式影像檢視器的設定屬性檔案。
seo-title: 命令參考——配置屬性
solution: Experience Manager
title: 命令參考——配置屬性
topic: Dynamic media
uuid: ef118730-1bd2-4b88-917c-1fa51c6a488b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 命令參考——配置屬性{#command-reference-configuration-attributes}

互動式影像檢視器的設定屬性檔案。

任何組態命令都可在URL中設定，或 `setParam()`使用或 `setParams()`同時使用API方法。 也可以在伺服器端組態記錄中指定任何組態屬性。

某些配置命令可能會加上類名或對應Viewer SDK元件的例項名稱前置詞。 元件的例項名稱是動態的，並視傳遞至 `setContainerId()` API方法的檢視器容器DOM元素ID而定。 說明檔案包含此類命令的可選首碼。 例如，命 `zoomstep` 令記錄如下：

`[ZoomView.|<containerId>_zoomView].fmt`

這表示您可以將此命令用作：

* `fmt` （簡短語法）
* `ZoomView.fmt` （限定元件類別名稱）
* `cont_zoomView.fmt` (以元件ID為限，假 `cont` 設是容器元素的ID)

另請參 [閱所有檢視器通用的命令參考——設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
