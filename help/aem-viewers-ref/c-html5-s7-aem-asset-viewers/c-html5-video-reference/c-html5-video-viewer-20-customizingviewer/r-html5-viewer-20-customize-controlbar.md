---
title: 控制列
description: 控制列是矩形區域，包含並位於所有可用於視訊檢視器的UI控制項後面，例如播放/暫停按鈕和音量控制項。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2239307a-4a05-4392-b35c-a64ea6c938ad
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---

# 控制列{#control-bar}

控制列是矩形區域，包含並位於所有可用於視訊檢視器的UI控制項後面，例如播放/暫停按鈕和音量控制項。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列總是取用整個可用的檢視器寬度。 您可以透過CSS變更其相對於視訊檢視器容器的顏色、高度和垂直位置。

下列CSS類別選擇器會控制控制列的外觀：

```
.s7videoviewer .s7controlbar
```

## 控制列的CSS屬性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 從下邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>控制列的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>控制列的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要設定具有灰色控制列的視訊檢視器，該控制列高度為30畫素，且位於視訊檢視器容器的頂端。

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
