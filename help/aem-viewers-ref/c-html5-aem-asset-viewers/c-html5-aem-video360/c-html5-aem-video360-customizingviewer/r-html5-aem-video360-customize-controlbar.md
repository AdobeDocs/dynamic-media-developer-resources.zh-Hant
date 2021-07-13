---
description: 控制欄是矩形區域，其中包含並位於視訊檢視器可用的所有使用者介面控制項，例如播放/暫停按鈕、音量控制項等。
solution: Experience Manager
title: 控制欄
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# 控制欄{#control-bar}

控制欄是矩形區域，其中包含並位於視訊檢視器可用的所有使用者介面控制項，例如播放/暫停按鈕、音量控制項等。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列一律會取用整個可用的檢視器寬度。 您可以透過CSS，相對於視訊檢視器容器來變更其顏色、高度和垂直位置。

以下CSS類選擇器控制控制欄的外觀：

```
.s7video360viewer .s7controlbar
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

**範例**  — 使用高度為30像素且位於視訊檢視器容器頂端的灰色控制列，設定視訊檢視器。

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
