---
description: 控制欄是矩形區域，其中包含並位於視訊檢視器可用的所有UI控制項，例如播放/暫停按鈕、音量控制項等。
solution: Experience Manager
title: 控制欄
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: 685fad5a-a75a-4c0c-9038-de99d814f4be
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# 控制欄{#control-bar}

控制欄是矩形區域，其中包含並位於視訊檢視器可用的所有UI控制項，例如播放/暫停按鈕、音量控制項等。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列一律會取用整個可用的檢視器寬度。 您可以透過CSS，相對於視訊檢視器容器來變更其顏色、高度和垂直位置。

以下CSS類選擇器控制控制欄的外觀：

```
.s7interactivevideoviewer .s7controlbar
```

## 控制欄的CSS屬性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 從底部邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>控制欄的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>控制欄的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定視訊檢視器，其灰色控制列高度為30像素，並位於視訊檢視器容器的頂端。

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
