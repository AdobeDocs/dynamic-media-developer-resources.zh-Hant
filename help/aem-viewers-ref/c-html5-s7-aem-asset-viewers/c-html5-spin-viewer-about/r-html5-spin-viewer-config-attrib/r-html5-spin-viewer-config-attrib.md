---
description: 回轉檢視器的設定屬性檔案。
seo-description: 回轉檢視器的設定屬性檔案。
seo-title: 命令參考——配置屬性
solution: Experience Manager
title: 命令參考——配置屬性
topic: Dynamic media
uuid: ba60da44-d30d-459f-b3d8-5cf3ea4bcbdb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# 命令參考——配置屬性{#command-reference-configuration-attributes}

回轉檢視器的設定屬性檔案。

任何組態命令都可在URL中設定，或使用`setParam()`或`setParams()`，或同時使用&lt;a1/>或兩者的API方法。 也可以在伺服器端組態記錄中指定任何組態屬性。

某些配置命令可能會加上類名或對應Viewer SDK元件的例項名稱前置詞。 元件的例項名稱是動態的，並視傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID而定。 說明檔案包含此類命令的可選首碼。 例如，`zoomstep`命令的說明如下：

`[SpinView.|<containerId>_spinView].zoomstep`

這表示您可以將此命令用作：

* `zoomstep` （簡短語法）
* `SpinView.zoomstep` （限定元件類別名稱）
* `cont_spinView.zoomstep` (以元件ID為限，假 `cont` 設是容器元素的ID)

另請參閱[所有查看器通用的命令參考——配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
