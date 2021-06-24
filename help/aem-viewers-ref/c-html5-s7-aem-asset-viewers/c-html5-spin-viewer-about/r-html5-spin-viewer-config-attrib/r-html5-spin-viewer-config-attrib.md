---
description: 回轉檢視器的設定屬性檔案。
solution: Experience Manager
title: 命令參考 — 配置屬性
feature: Dynamic Media Classic，檢視器，SDK/API，回轉集
role: Developer,Business Practitioner
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# 命令參考 — 配置屬性{#command-reference-configuration-attributes}

回轉檢視器的設定屬性檔案。

任何設定命令都可在URL中設定，或使用`setParam()`、`setParams()`或兩者，API方法。 也可在伺服器端設定記錄中指定任何設定屬性。

某些設定命令的前置詞可能是對應檢視器SDK元件的類別名稱或執行個體名稱。 元件的例項名稱為動態，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID。 文檔中包含此類命令的可選前置詞。 例如， `zoomstep`命令記錄如下：

`[SpinView.|<containerId>_spinView].zoomstep`

這表示您可以將此命令用作：

* `zoomstep` （簡短語法）
* `SpinView.zoomstep` （以元件類名稱限定）
* `cont_spinView.zoomstep` (以元件ID為限，假 `cont` 設為容器元素的ID)

另請參閱[所有檢視器通用的命令參考 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
