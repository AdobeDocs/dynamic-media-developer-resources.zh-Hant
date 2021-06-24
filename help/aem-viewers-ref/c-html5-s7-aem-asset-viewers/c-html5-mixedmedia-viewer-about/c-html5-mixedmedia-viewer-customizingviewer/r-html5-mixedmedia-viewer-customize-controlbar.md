---
description: 控制欄是矩形區域，其中包含並位於視訊檢視器可用的所有使用者介面控制項，例如播放/暫停按鈕、音量控制項等。
solution: Experience Manager
title: 控制欄
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# 控制欄{#control-bar}

控制欄是矩形區域，其中包含並位於視訊檢視器可用的所有使用者介面控制項，例如播放/暫停按鈕、音量控制項等。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列一律會取用整個可用的檢視器寬度。 您可以透過CSS，相對於視訊檢視器容器來變更其顏色、高度和垂直位置。

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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>控制欄的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定混合媒體檢視器，並搭配高度為30像素的灰色控制列。

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
