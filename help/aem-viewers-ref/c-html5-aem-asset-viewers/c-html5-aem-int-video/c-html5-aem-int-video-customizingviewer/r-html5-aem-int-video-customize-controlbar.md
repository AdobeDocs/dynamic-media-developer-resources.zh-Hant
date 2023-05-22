---
title: 控制欄
description: 控制欄是矩形區域，包含並位於視頻查看器可用的所有用戶介面控制項（如播放/暫停按鈕和音量控制項）的後面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 685fad5a-a75a-4c0c-9038-de99d814f4be
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# 控制欄{#control-bar}

控制欄是矩形區域，包含並位於視頻查看器可用的所有用戶介面控制項（如播放/暫停按鈕和音量控制項）的後面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制欄始終取整個可用查看器寬度。 可以通過CSS相對於視頻查看器容器更改其顏色、高度和垂直位置。

以下CSS類選擇器控制控制欄的外觀：

```
.s7interactivevideoviewer .s7controlbar
```

## 控制欄的CSS屬性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從上邊框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 從底邊框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>控制欄的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>控制欄的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定一個帶有30像素高且位於視頻查看器容器頂部的灰色控制欄的視頻查看器。

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
