---
title: 命令參考 — 配置屬性
description: 智慧型裁切視訊檢視器的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# 命令參考 — 配置屬性{#command-reference-configuration-attributes}

智慧型裁切視訊檢視器的設定屬性檔案。

您可以在URL中設定任何設定命令。 或者，您可以使用API方法 `setParam()`，或 `setParams()`，或兩者，以設定任何設定命令。 您也可以在伺服器端設定記錄中指定任何設定屬性。

您可以為某些設定命令加上類別名稱或對應檢視器SDK元件的執行個體名稱前置詞。 元件的例項名稱為動態，且取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` API方法。 文檔包括此類命令的可選前置詞。 例如， `playback` 如下所述：

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

這表示此命令的使用方式如下：

* `playback` （簡短語法）
* `SmartCropVideoPlayer.playback` （以元件類名稱限定）
* `cont_videoPlayer.playback` (以元件ID限定，假設 `cont` 是容器元素的ID)

請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

請參閱 [所有檢視器 — URL通用的命令參考](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
