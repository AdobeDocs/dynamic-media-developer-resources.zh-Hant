---
description: 控制列是矩形區域，包含並位於影片檢視器可用的所有UI控制項後方，例如播放／暫停按鈕、音量控制項等。
seo-description: 控制列是矩形區域，包含並位於影片檢視器可用的所有UI控制項後方，例如播放／暫停按鈕、音量控制項等。
seo-title: 控制列
solution: Experience Manager
title: 控制列
uuid: 5686b670-3c8c-4bef-b428-dc468f6ca05d
feature: Dynamic Media經典，檢視器，SDK/API，視訊
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---


# 控制列{#control-bar}

控制列是矩形區域，包含並位於影片檢視器可用的所有UI控制項後方，例如播放／暫停按鈕、音量控制項等。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列一律會取用整個可用的檢視器寬度。 您可以透過CSS相對於視訊檢視器容器來變更其顏色、高度和垂直位置。

下列CSS類別選擇器會控制控制列的外觀：

```
.s7videoviewer .s7controlbar
```

## 控制列{#css-properties-of-the-control-bar}的CSS屬性

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從上邊框的位置，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 從底部邊框的位置，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>控制列的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>控制列的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要設定視訊檢視器，其灰色控制列高度為30像素，並位於視訊檢視器容器的頂端。

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

