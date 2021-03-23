---
description: 縮放檢視器的設定屬性檔案。
seo-description: 縮放檢視器的設定屬性檔案。
seo-title: 命令參考——配置屬性
solution: Experience Manager
title: 命令參考——配置屬性
uuid: 1bcc879a-12ec-4924-ac05-2e4c1d6e4597
feature: Dynamic Media經典，檢視器，SDK/API，縮放
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# 命令參考——配置屬性{#command-reference-configuration-attributes}

縮放檢視器的設定屬性檔案。

任何組態命令都可在URL中設定，或使用`setParam()`或`setParams()`，或同時使用或兩者的API方法。 也可以在伺服器端組態記錄中指定任何組態屬性。

某些配置命令可能會加上類名或對應Viewer SDK元件的例項名稱前置詞。 元件的例項名稱是動態的，並視傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID而定。 說明檔案包含此類命令的可選首碼。 例如，`zoomstep`命令的說明如下：

`[ZoomView.|<containerId>_zoomView].zoomstep`

這表示您可以將此命令用作：

* `zoomstep` （簡短語法）
* `ZoomView.zoomstep` （限定元件類別名稱）
* `cont_zoomView.zoomstep` (以元件ID為限，假 `cont` 設是容器元素的ID)

另請參閱[所有查看器通用的命令參考——配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
