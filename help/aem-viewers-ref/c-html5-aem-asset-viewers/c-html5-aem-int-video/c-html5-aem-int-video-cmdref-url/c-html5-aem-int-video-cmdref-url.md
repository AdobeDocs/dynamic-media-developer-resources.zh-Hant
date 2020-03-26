---
description: 互動式視訊檢視器的指令參考檔案。
seo-description: 互動式視訊檢視器的指令參考檔案。
seo-title: 命令參考- URL
solution: Experience Manager
title: 命令參考- URL
topic: Dynamic media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
translation-type: tm+mt
source-git-commit: 3266e8682711dac379a09a0e992d33b8ffc7b5a4

---


# 命令參考- URL{#command-reference-url}

互動式視訊檢視器的指令參考檔案。

您可以在URL中設定任何組態命令。 或者，您可以使用API方法 `setParam()`或/ `setParams()`或兩者來設定任何組態命令。 您也可以在伺服器端組態記錄中指定任何組態屬性。

您可以在某些配置命令的前置詞中加上類別名稱或對應Viewer SDK元件的例項名稱。 元件的例項名稱是動態的，並視傳遞至 `setContainerId()` API方法的檢視器容器DOM元素ID而定。 文檔包括這些命令的可選前置詞。 例如， `playback` 說明如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

這表示以下方式使用此命令：

* `playback` （簡短語法）
* `VideoPlayer.playback` （限定元件類別名稱）
* `cont_videoPlayer.playback` (以元件ID為限，假設 `cont` 是容器元素的ID)

另請參 [閱所有檢視器通用的命令參考——設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)。

另請參 [閱所有檢視器- URL通用的命令參考](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)。
