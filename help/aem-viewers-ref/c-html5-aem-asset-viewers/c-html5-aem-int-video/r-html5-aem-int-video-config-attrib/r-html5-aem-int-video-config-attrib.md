---
title: 命令參考 — 配置屬性
description: 互動式視訊檢視器的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 80b7971c-82dc-47a2-adde-9e061a0f856d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# 命令參考 — 配置屬性{#command-reference-configuration-attributes}

互動式視訊檢視器的設定屬性檔案。

任何設定命令都可在URL中設定，或使用`setParam()`、`setParams()`或兩者，API方法。 也可在伺服器端設定記錄中指定任何設定屬性。

某些設定命令的前置詞可能是對應檢視器SDK元件的類別名稱或執行個體名稱。 元件的例項名稱為動態，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID。 文檔中包含此類命令的可選前置詞。 例如， `playback`命令記錄如下：

`[VideoPlayer.|<containerId>_videoPlayer].playback`

也就是說，您可以將下列命令用作：

* `playback` （簡短語法）
* `VideoPlayer.playback` （以元件類名稱限定）
* `cont_videoPlayer.playback` (以元件ID為限，假 `cont` 設為容器元素的ID)

另請參閱[所有檢視器通用的命令參考 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
