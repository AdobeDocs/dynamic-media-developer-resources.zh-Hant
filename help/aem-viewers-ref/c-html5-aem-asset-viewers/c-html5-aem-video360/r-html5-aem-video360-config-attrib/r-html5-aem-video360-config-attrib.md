---
title: 命令引用 — 配置屬性
description: Video360 Viewer的配置屬性文檔。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令引用 — 配置屬性{#command-reference-configuration-attributes}

Video360 Viewer的配置屬性文檔。

可以在URL中或使用 `setParam()`或 `setParams()`或兩者兼有的API方法。 也可以在伺服器端配置記錄中指定任何配置屬性。

某些配置命令可能以相應Viewer SDK元件的類名或實例名為前置詞。 元件的實例名稱是動態的，取決於傳遞給的查看器容器DOM元素的ID `setContainerId()` API方法。 文檔中包含此類命令的可選前置詞。 比如說， `playback` 命令的說明如下：

`[VideoPlayer.|<containerId>_videoPlayer].playback`

這意味著您可以在以下命令中使用此命令：

* `playback` （短語法）
* `VideoPlayer.playback` （使用元件類名限定）
* `cont_videoPlayer.playback` (使用元件ID限定，假定 `cont` 是容器元素的ID)

另請參閱 [所有查看器通用的命令引用 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
