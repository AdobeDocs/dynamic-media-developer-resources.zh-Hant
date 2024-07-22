---
title: 命令參考 — URL
description: 視訊檢視器的命令參考檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1ed78e0d-9b93-4c66-b558-fac15c51e944
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# 命令參考 — URL{#command-reference-url}

視訊檢視器的命令參考檔案。

您可以在URL中設定任何組態命令。 或者，您可以使用API方法`setParam()`或`setParams()`，或兩者來設定任何組態命令。 您也可以在伺服器端組態記錄中指定任何組態屬性。

您可以使用類別名稱或相對應的Viewer SDK元件的例項名稱為某些組態命令加上前置詞。 元件的執行個體名稱是動態的，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素的識別碼。 說明檔案包含這類命令的選用首碼。 例如，`playback`的記錄如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

這表示此指令的用途如下

* `playback` （簡短語法）
* `VideoPlayer.playback` （以元件類別名稱限定）
* `cont_videoPlayer.playback` （以元件ID限定，假設`cont`是容器元素的識別碼）

另請參閱[所有檢視器通用的命令參考 — 組態屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)。

另請參閱所有檢視器通用的[命令參考 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)。
