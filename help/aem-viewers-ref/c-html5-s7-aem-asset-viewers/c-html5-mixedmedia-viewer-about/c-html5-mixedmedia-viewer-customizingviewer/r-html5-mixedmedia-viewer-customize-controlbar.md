---
description: 控制列是矩形區域，包含並位於影片檢視器可用的所有使用者介面控制項（例如播放／暫停按鈕、音量控制項等）後面。
solution: Experience Manager
title: 控制列
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# 控制列{#control-bar}

控制列是矩形區域，包含並位於影片檢視器可用的所有使用者介面控制項（例如播放／暫停按鈕、音量控制項等）後面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列一律會取用整個可用的檢視器寬度。 您可以透過CSS相對於視訊檢視器容器來變更其顏色、高度和垂直位置。

下列CSS類別選擇器會控制控制列的外觀：

```
.s7mixedmediaviewer .s7controlbar
```

## 控制列{#css-properties-of-the-control-bar}的CSS屬性

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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

若要設定高度為30像素的灰色控制列的混合媒體檢視器。

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

