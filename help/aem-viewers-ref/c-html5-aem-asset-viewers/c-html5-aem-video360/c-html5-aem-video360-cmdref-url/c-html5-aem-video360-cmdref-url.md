---
title: 命令引用 — URL
description: Video360 Viewer的命令參考文檔。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# 命令引用 — URL{#command-reference-url}

Video360 Viewer的命令參考文檔。

可以在URL中設定任何配置命令。 或者，可以使用API方法 `setParam()`或 `setParams()`或同時設定任何配置命令。 也可以在伺服器端配置記錄中指定任何config屬性。

可以用類名或相應的HTML5 Viewer SDK元件的實例名為某些配置命令前置詞。 元件的實例名稱是動態的，取決於傳遞給的查看器容器DOM元素的ID `setContainerId()` API方法。 文檔包括此類命令的可選前置詞。 比如說， `playback` 如下所述：

```
[Video360Player.|<containerId>_video360Player].playback
```

這表示此命令的使用方式如下：

* `playback` （短語法）
* `Video360Player.playback` （使用元件類名限定）
* `cont_video360Player.playback` (使用元件ID限定，假定 `cont` 是容器元素的ID)

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
