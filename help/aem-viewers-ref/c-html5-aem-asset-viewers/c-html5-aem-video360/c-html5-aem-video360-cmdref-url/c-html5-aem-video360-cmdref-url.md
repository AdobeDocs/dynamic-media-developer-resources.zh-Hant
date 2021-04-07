---
description: Video360檢視器的指令參考檔案。
solution: Experience Manager
title: 命令參考- URL
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# 命令參考- URL{#command-reference-url}

Video360檢視器的指令參考檔案。

您可以在URL中設定任何組態命令。 或者，您可以使用API方法`setParam()`或`setParams()`，或兩者來設定任何組態命令。 您也可以在伺服器端組態記錄中指定任何組態屬性。

您可以在某些配置命令的前置詞中加上類名或對應HTML5檢視器SDK元件的例項名。 元件的例項名稱是動態的，並視傳遞至`setContainerId()` API方法的檢視器容器DOM元素ID而定。 文檔包括這些命令的可選前置詞。 例如，`playback`的說明如下：

```
[Video360Player.|<containerId>_video360Player].playback
```

這表示以下方式使用此命令：

* `playback` （簡短語法）
* `Video360Player.playback` （限定元件類別名稱）
* `cont_video360Player.playback` (以元件ID為限，假設 `cont` 是容器元素的ID)

請參閱所有檢視器通用的[命令參考——設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和[所有檢視器通用的命令參考- URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
