---
title: 命令引用 — 配置屬性
description: Panoramic Viewer的配置屬性文檔。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# 命令引用 — 配置屬性{#command-reference-configuration-attributes}

Panoramic Viewer的配置屬性文檔。

可以在URL中或使用 `setParam()` 和/或 `setParams()` API方法。 也可以在伺服器端配置記錄中指定任何配置屬性。

某些配置命令可以用相應HTML5 SDK元件的類名或實例名前置詞。 元件的實例名稱是動態的，取決於傳遞給的查看器容器DOM元素的ID `setContainerId()` API方法。 文檔將包括此類命令的可選前置詞。 比如說， `vrrender` 命令的說明如下：

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

這意味著此命令的使用方式如下：

* `vrrender` （短語法）
* `PanoramicView.vrrender` （使用元件類名限定）
* `cont_panoramicView.vrrender` （使用元件ID限定，假定cont是容器元素的ID）


請參閱 [所有查看器通用的命令引用 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

請參閱 [所有查看器通用的命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
