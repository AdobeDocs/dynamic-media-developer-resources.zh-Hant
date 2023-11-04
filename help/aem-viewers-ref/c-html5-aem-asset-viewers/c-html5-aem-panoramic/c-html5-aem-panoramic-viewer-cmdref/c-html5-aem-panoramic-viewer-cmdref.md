---
title: 命令參考 — 組態屬性
description: 全景檢視器的組態屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

全景檢視器的組態屬性檔案。

任何設定命令都可以在URL中設定，或使用 `setParam()` 和/或 `setParams()` API方法。 任何設定屬性也可在伺服器端設定記錄中指定。

某些設定命令可能會加上對應HTML5 SDK元件的類別名稱或例項名稱當作前置詞。 元件的例項名稱是動態的，取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` API方法。 檔案包含這類命令的選用首碼。 例如， `vrrender` 命令記錄如下：

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

這表示此指令的使用方式如下：

* `vrrender` （簡短語法）
* `PanoramicView.vrrender` （以元件類別名稱限定）
* `cont_panoramicView.vrrender` （限定為元件ID，假設續為容器元素的ID）


另請參閱 [所有檢視器通用的命令參考 — 組態屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

另請參閱 [所有檢視器通用的命令參考 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
