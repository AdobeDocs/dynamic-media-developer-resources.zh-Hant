---
title: 全景檢視器
description: 建構函式，建立HTML5全景檢視器例項。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:09:54.686Z'
TQID: 'https://experienceleague.adobe.com/zSYqLmLn-LQhkIIrPe31JIouevTWijICBcrmY3fol1M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%
---
# 全景檢視器{#panoramicviewer}

`PanoramicViewer([config])`
建構函式，建立HTML5全景檢視器例項。

## 參數 {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object}選用的JSON設定物件，可讓您將所有檢視器設定傳遞至建構函式，並避免呼叫個別setter方法。 它包含下列屬性：

* containerId — 檢視器插入的DOM容器（通常是DIV）的{String}識別碼。 不需要在呼叫此方法時建立container元素，但是執行init()時容器必須存在。 必要
* params — 具有檢視器組態引數的{Object} JSON物件，其中屬性名稱是檢視器特定的組態選項或SDK修飾元，且該屬性的值是對應的設定值。 必要
* 處理常式 — 具有檢視器事件回呼的{Object} JSON物件，其中屬性名稱是支援的檢視器事件的名稱，屬性值是適當回呼的JavaScript函式參考。 如需檢視器事件的詳細資訊，請參閱事件回呼區段。 選擇性.


## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
