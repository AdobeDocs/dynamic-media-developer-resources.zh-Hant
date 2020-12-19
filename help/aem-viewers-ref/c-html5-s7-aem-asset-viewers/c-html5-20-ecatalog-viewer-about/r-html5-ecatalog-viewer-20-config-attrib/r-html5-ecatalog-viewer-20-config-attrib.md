---
description: eCatalog檢視器的設定屬性檔案。
seo-description: eCatalog檢視器的設定屬性檔案。
seo-title: 命令參考——配置屬性
solution: Experience Manager
title: 命令參考——配置屬性
topic: Dynamic media
uuid: 823ad411-653a-44de-97de-147e3b27a917
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# 命令參考——配置屬性{#command-reference-configuration-attributes}

eCatalog檢視器的設定屬性檔案。

任何組態命令都可在URL中設定，或使用`setParam()`或`setParams()`，或同時使用&lt;a1/>或兩者的API方法。 您也可以指定伺服器端組態記錄中指定的任何組態屬性。

對於某些配置命令，您可在其前置詞上加上對應Viewer SDK元件的類別名稱或例項名稱。 元件的例項名稱是動態的，並視傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID而定。 說明檔案包含此類命令的可選首碼。 例如，`zoomstep`命令的說明如下：

`[PageView.|<containerId>_pageView].zoomstep`

這表示您可以將此命令用作：

* `zoomstep` （簡短語法）
* `PageView.zoomstep` （限定元件類別名稱）
* `cont_pageView.zoomstep` (以元件ID為限，假 `cont` 設是容器元素的ID)

另請參閱[所有查看器通用的命令參考——配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
