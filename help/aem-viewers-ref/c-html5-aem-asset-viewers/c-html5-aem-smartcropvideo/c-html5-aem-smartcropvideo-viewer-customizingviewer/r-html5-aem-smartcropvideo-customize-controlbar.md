---
title: 控制欄
description: 控制欄是矩形區域，包含並位於Smart Crop視頻查看器可用的所有UI控制項（如播放/暫停按鈕和音量控制項）的後面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 8ea06e0a-705d-436a-9393-75a36381cba6
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# 控制欄{#control-bar}

控制欄是矩形區域，包含並位於Smart Crop視頻查看器可用的所有UI控制項（如播放/暫停按鈕和音量控制項）的後面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制欄始終取整個可用查看器寬度。 通過CSS可以相對於Smart Crop Video查看器容器更改其顏色、高度和垂直位置。

以下CSS類選擇器控制控制欄的外觀：

```
.s7smartcropvideoviewer .s7controlbar
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

設定Smart Crop視頻查看器，其灰色控制欄高30像素，位於Smart Crop視頻查看器容器的頂部。

```
.s7smartcropvideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
