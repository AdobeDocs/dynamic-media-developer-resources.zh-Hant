---
title: 命令參考 — 配置屬性
description: 縮放檢視器的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 命令參考 — 配置屬性{#command-reference-configuration-attributes}

縮放檢視器的設定屬性檔案。

任何設定命令皆可在URL中設定，或使用 `setParam()`，或 `setParams()`、或兩者， API方法。 也可在伺服器端設定記錄中指定任何設定屬性。

某些設定命令的前置詞可能是對應檢視器SDK元件的類別名稱或執行個體名稱。 元件的例項名稱為動態，且取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` API方法。 文檔中包含此類命令的可選前置詞。 例如， `zoomstep` 命令記錄如下：

`[ZoomView.|<containerId>_zoomView].zoomstep`

這表示您可以將命令用作

* `zoomstep` （簡短語法）
* `ZoomView.zoomstep` （以元件類名稱限定）
* `cont_zoomView.zoomstep` (以元件ID限定，假設為 `cont` 是容器元素的ID)

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
