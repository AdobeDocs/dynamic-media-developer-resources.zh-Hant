---
description: eCatalog檢視器的設定屬性檔案。
solution: Experience Manager
title: 命令參考 — 配置屬性
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# 命令參考 — 配置屬性{#command-reference-configuration-attributes}

eCatalog檢視器的設定屬性檔案。

任何設定命令都可在URL中設定，或使用`setParam()`、`setParams()`或兩者，API方法。 您也可以指定伺服器端設定記錄中指定的任何設定屬性。

對於某些設定命令，您可以在其前面加上對應檢視器SDK元件的類別名稱或例項名稱。 元件的例項名稱為動態，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID。 文檔中包含此類命令的可選前置詞。 例如， `zoomstep`命令記錄如下：

`[PageView.|<containerId>_pageView].zoomstep`

這表示您可以將此命令用作：

* `zoomstep` （簡短語法）
* `PageView.zoomstep` （以元件類名稱限定）
* `cont_pageView.zoomstep` (以元件ID為限，假 `cont` 設為容器元素的ID)

另請參閱[所有檢視器通用的命令參考 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
