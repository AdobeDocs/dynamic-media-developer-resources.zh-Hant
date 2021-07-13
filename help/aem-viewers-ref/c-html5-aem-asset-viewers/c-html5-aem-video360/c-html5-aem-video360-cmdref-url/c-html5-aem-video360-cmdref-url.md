---
description: Video360查看器的命令參考文檔。
solution: Experience Manager
title: 命令參考 — URL
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 命令參考 — URL{#command-reference-url}

Video360查看器的命令參考文檔。

您可以在URL中設定任何設定命令。 或者，您也可以使用API方法`setParam()`或`setParams()`，或兩者來設定任何設定命令。 您也可以在伺服器端設定記錄中指定任何設定屬性。

您可以為某些設定命令加上類別名稱或對應HTML5檢視器SDK元件之例項名稱的前置詞。 元件的例項名稱為動態，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID。 文檔包括此類命令的可選前置詞。 例如， `playback`記錄如下：

```
[Video360Player.|<containerId>_video360Player].playback
```

這表示此命令的使用方式如下：

* `playback` （簡短語法）
* `Video360Player.playback` （以元件類名稱限定）
* `cont_video360Player.playback` (以元件ID為限，假 `cont` 設為容器元素的ID)

請參閱所有檢視器通用的[命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
