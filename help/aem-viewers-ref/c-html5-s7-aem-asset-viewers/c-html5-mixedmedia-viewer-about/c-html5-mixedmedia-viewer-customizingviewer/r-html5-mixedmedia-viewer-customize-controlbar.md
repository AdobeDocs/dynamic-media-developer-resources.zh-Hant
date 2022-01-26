---
title: 控制欄
description: 控制欄是矩形區域，包含並位於視頻查看器可用的所有用戶介面控制項（如「播放/暫停」按鈕、音量控制項等）的後面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---

# 控制欄{#control-bar}

控制欄是矩形區域，包含並位於視頻查看器可用的所有用戶介面控制項（如「播放/暫停」按鈕、音量控制項等）的後面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制欄始終取整個可用查看器寬度。 可以通過CSS相對於視頻查看器容器更改其顏色、高度和垂直位置。

以下CSS類選擇器控制控制欄的外觀：

```
.s7mixedmediaviewer .s7controlbar
```

## 控制欄的CSS屬性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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

設定帶有30像素高的灰色控制欄的混合媒體查看器。

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
