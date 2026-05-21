---
title: 控制列
description: 控制列是矩形的區域，其中包含並位於所有可用於視訊檢視器的使用者介面控制項後面，例如播放/暫停按鈕和音量控制項。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 685fad5a-a75a-4c0c-9038-de99d814f4be
TQID: 'https://experienceleague.adobe.com/1tSWpSM3wPGihSid3WocaUo8HD6BP4arexuws5XRTPA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 0%

---

# 控制列{#control-bar}

控制列是矩形的區域，其中包含並位於所有可用於視訊檢視器的使用者介面控制項後面，例如播放/暫停按鈕和音量控制項。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列一律採用完整的可用檢視器寬度。 您可以透過CSS變更其相對於視訊檢視器容器的顏色、高度和垂直位置。

下列CSS類別選取器會控制控制列的外觀：

```
.s7interactivevideoviewer .s7controlbar
```

## 控制列的CSS屬性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">後</span> </p> </td> 
   <td colname="col2"> <p> 從下邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>控制列的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>控制列的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定具有30畫素高且位於視訊檢視器容器頂端的灰色控制列的視訊檢視器。

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
