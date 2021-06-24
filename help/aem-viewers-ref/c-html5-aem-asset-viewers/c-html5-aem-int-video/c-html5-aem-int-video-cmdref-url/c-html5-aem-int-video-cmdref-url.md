---
description: 互動式視訊檢視器的命令參考檔案。
solution: Experience Manager
title: 命令參考 — URL
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: e0a9e269-4826-4518-9222-6a833d11746b
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# 命令參考 — URL{#command-reference-url}

互動式視訊檢視器的命令參考檔案。

您可以在URL中設定任何設定命令。 或者，您也可以使用API方法`setParam()`或`setParams()`，或兩者來設定任何設定命令。 您也可以在伺服器端設定記錄中指定任何設定屬性。

您可以為某些設定命令加上類別名稱或對應檢視器SDK元件的執行個體名稱前置詞。 元件的例項名稱為動態，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID。 文檔包括此類命令的可選前置詞。 例如， `playback`記錄如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

這表示此命令的使用方式如下：

* `playback` （簡短語法）
* `VideoPlayer.playback` （以元件類名稱限定）
* `cont_videoPlayer.playback` (以元件ID為限，假 `cont` 設為容器元素的ID)

另請參閱[所有檢視器通用的命令參考 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)。

另請參閱[所有檢視器通用的命令參考 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)。
