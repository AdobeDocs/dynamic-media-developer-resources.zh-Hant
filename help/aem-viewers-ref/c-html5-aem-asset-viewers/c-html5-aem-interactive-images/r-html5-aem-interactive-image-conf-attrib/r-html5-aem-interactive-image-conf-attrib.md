---
description: 互動式影像檢視器的設定屬性檔案。
solution: Experience Manager
title: 命令參考 — 配置屬性
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影像
role: Developer,Business Practitioner
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# 命令參考 — 配置屬性{#command-reference-configuration-attributes}

互動式影像檢視器的設定屬性檔案。

任何設定命令都可在URL中設定，或使用`setParam()`、`setParams()`或兩者，API方法。 也可在伺服器端設定記錄中指定任何設定屬性。

某些設定命令的前置詞可能是對應檢視器SDK元件的類別名稱或執行個體名稱。 元件的例項名稱為動態，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID。 文檔中包含此類命令的可選前置詞。 例如， `zoomstep`命令記錄如下：

`[ZoomView.|<containerId>_zoomView].fmt`

這表示您可以將此命令用作：

* `fmt` （簡短語法）
* `ZoomView.fmt` （以元件類名稱限定）
* `cont_zoomView.fmt` (以元件ID為限，假 `cont` 設為容器元素的ID)

另請參閱[所有檢視器通用的命令參考 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
