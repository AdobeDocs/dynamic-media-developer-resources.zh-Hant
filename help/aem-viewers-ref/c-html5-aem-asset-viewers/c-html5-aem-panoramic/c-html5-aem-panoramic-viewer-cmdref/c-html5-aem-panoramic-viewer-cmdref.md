---
title: 命令參考 — 配置屬性
description: 全景檢視器的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 6118fac8a41abaf5db150820b982bec5bc45f0ff
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# 命令參考 — 配置屬性{#command-reference-configuration-attributes}

全景檢視器的設定屬性檔案。

任何設定命令皆可在URL中設定，或使用 `setParam()` 和/或 `setParams()` API方法。 也可在伺服器端設定記錄中指定任何設定屬性。

某些設定命令的前置詞可能是對應HTML5 SDK元件的類別名稱或執行個體名稱。 元件的例項名稱為動態，且取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` API方法。 文檔將包含此類命令的可選前置詞。 例如， `vrrender` 命令將記錄如下：

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

這表示此命令的使用方式如下：

* `vrrender` （簡短語法）
* `PanoramicView.vrrender` （以元件類名稱限定）
* `cont_panoramicView.vrrender` （以元件ID為限，假設cont為容器元素的ID）


請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

請參閱 [所有檢視器 — URL通用的命令參考](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
