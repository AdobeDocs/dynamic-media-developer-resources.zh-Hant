---
title: 命令參考 — 組態屬性
description: 縮放檢視器的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
TQID: 'https://experienceleague.adobe.com/34VqWl1GOWOG7G8vXJIpc7NH4w26x2NOGO3yG2yknyc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

縮放檢視器的設定屬性檔案。

任何設定命令都可以在URL中設定，或使用`setParam()`、`setParams()`或兩者的API方法設定。 任何設定屬性也可在伺服器端設定記錄中指定。

某些設定命令可能會加上相對應檢視器SDK元件的類別名稱或例項名稱當作前置詞。 元件的執行個體名稱是動態的，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素的識別碼。 檔案包含這類命令的選用首碼。 例如，`zoomstep`命令的記錄如下：

`[ZoomView.|<containerId>_zoomView].zoomstep`

這表示您可以使用指令作為

* `zoomstep` （簡短語法）
* `ZoomView.zoomstep` （以元件類別名稱限定）
* `cont_zoomView.zoomstep` （以元件ID限定，假設`cont`是容器元素的識別碼）

另請參閱所有檢視者通用的[命令參考 — 組態屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

