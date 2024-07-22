---
title: 命令參考 — 組態屬性
description: Video360 Viewer的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

Video360 Viewer的設定屬性檔案。

任何設定命令都可以在URL中設定，或使用`setParam()`、`setParams()`或兩者的API方法設定。 任何組態屬性也可在伺服器端組態記錄中指定。

某些設定命令可能會加上相對應Viewer SDK元件的類別名稱或例項名稱當作前置詞。 元件的執行個體名稱是動態的，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素的識別碼。 檔案包含這類命令的選用首碼。 例如，`playback`命令的記錄如下：

`[VideoPlayer.|<containerId>_videoPlayer].playback`

這表示您可以在下列專案中使用這個指令：

* `playback` （簡短語法）
* `VideoPlayer.playback` （以元件類別名稱限定）
* `cont_videoPlayer.playback` （以元件ID限定，假設`cont`是容器元素的識別碼）

另請參閱所有檢視者通用的[命令參考 — 組態屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
