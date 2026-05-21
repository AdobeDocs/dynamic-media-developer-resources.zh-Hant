---
title: 命令參考 — 組態屬性
description: eCatalog檢視器的組態屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
TQID: 'https://experienceleague.adobe.com/NRcFJ2RyskUxLayfdSmJ-jk-rHjPWiOWt0XwQJ7tvM8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

eCatalog檢視器的組態屬性檔案。

任何設定命令都可以在URL中設定，或使用`setParam()`、`setParams()`或兩者的API方法設定。 您也可以指定伺服器端組態記錄中指定的任何組態屬性。

對於某些組態命令，您可以使用對應Viewer SDK元件的類別名稱或例項名稱做為前置詞。 元件的執行個體名稱是動態的，且取決於傳遞至`setContainerId()` API方法的檢視器容器DOM元素的識別碼。 檔案包含這類命令的選用首碼。 例如，`zoomstep`命令的記錄如下：

`[PageView.|<containerId>_pageView].zoomstep`

這表示您可以將此指令用作

* `zoomstep` （簡短語法）
* `PageView.zoomstep` （以元件類別名稱限定）
* `cont_pageView.zoomstep` （以元件ID限定，假設`cont`是容器元素的識別碼）

另請參閱所有檢視者通用的[命令參考 — 組態屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
