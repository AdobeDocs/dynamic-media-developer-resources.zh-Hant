---
title: 控制欄
description: 控制欄是矩形區域，包含並位於智慧型裁切視訊檢視器可用的所有UI控制項（例如播放/暫停按鈕和音量控制項）後面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# 控制欄{#control-bar}

控制欄是矩形區域，包含並位於智慧型裁切視訊檢視器可用的所有UI控制項（例如播放/暫停按鈕和音量控制項）後面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列一律會取用整個可用的檢視器寬度。 您可以透過CSS，相對於智慧型裁切視訊檢視器容器來變更其顏色、高度和垂直位置。

以下CSS類選擇器控制控制欄的外觀：

```
.s7smartcropvideoviewer .s7controlbar
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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色 </span> </p> </td> 
   <td colname="col2"> <p>控制欄的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定具有30像素高且位於智慧型裁切視訊檢視器容器頂端的灰色控制列的智慧型裁切視訊檢視器。

```
.s7smartcropvideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
