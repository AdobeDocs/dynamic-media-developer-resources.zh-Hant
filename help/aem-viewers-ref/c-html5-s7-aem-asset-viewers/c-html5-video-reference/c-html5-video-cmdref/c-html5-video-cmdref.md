---
description: 視訊檢視器的設定屬性檔案。
seo-description: 視訊檢視器的設定屬性檔案。
seo-title: 命令參考——配置屬性
solution: Experience Manager
title: 命令參考——配置屬性
topic: Dynamic media
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 命令參考——配置屬性{#command-reference-configuration-attributes}

視訊檢視器的設定屬性檔案。

您可以在URL中設定任何組態命令。 或者，您可以使用API方法 `setParam()`或/ `setParams()`或兩者來設定任何組態命令。 您也可以在伺服器端組態記錄中指定任何組態屬性。

您可以在某些配置命令的前置詞中加上類別名稱或對應Viewer SDK元件的例項名稱。 元件的例項名稱是動態的，並視傳遞至 `setContainerId()` API方法的檢視器容器DOM元素ID而定。 文檔包括這些命令的可選前置詞。 例如， `playback` 說明如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

這表示以下方式使用此命令：

* `playback` （簡短語法）
* `VideoPlayer.playback` （限定元件類別名稱）
* `cont_videoPlayer.playback` (以元件ID為限，假設 `cont` 是容器元素的ID)

請參 [閱所有檢視器通用的命令參考——設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

請參 [閱所有檢視器通用的命令參考- URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
