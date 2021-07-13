---
description: Flyout檢視器的設定屬性檔案
solution: Experience Manager
title: 命令參考 — 配置屬性
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# 命令參考 — 配置屬性{#command-reference-configuration-attributes}

Flyout檢視器的設定屬性檔案

您可以在URL中設定任何設定命令。 或者，您可以使用`setParam()`、`setParams()`或兩種API方法。 您也可以在伺服器端設定記錄中指定任何設定屬性。

某些設定命令的前置詞為對應檢視器SDK元件的類別名稱或執行個體名稱。 元件的例項名稱為動態，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID。 文檔中包含此類命令的可選前置詞。 例如， `zoomfactor`命令記錄如下：

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

該命令的用法如下：

* `zoomfactor` （簡短語法）
* `FlyoutZoomView.zoomfactor` （用元件類名稱限定）
* `cont_flyout.zoomfactor` (以元件ID為限，假 `cont` 設為容器元素的ID)

另請參閱[所有檢視器通用的命令參考 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
