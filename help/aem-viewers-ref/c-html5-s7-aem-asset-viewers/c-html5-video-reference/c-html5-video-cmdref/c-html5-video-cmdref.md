---
title: 命令引用 — 配置屬性
description: 視頻查看器的配置屬性文檔。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# 命令引用 — 配置屬性{#command-reference-configuration-attributes}

視頻查看器的配置屬性文檔。

可以在URL中設定任何配置命令。 或者，可以使用API方法 `setParam()`或 `setParams()`或同時設定任何配置命令。 也可以在伺服器端配置記錄中指定任何config屬性。

可以使用類名或相應Viewer SDK元件的實例名來為某些配置命令添加前置詞。 元件的實例名稱是動態的，取決於傳遞給的查看器容器DOM元素的ID `setContainerId()` API方法。 文檔包括此類命令的可選前置詞。 比如說， `playback` 如下所述：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

這意味著此命令的使用方式如下

* `playback` （短語法）
* `VideoPlayer.playback` （使用元件類名限定）
* `cont_videoPlayer.playback` (使用元件ID限定，假定 `cont` 是容器元素的ID)

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

請參閱 [所有查看器通用的命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
