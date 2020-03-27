---
description: 主要檢視區域被視訊佔據。 當未指定大小時，通常會設定為符合可用的裝置畫面。
seo-description: 主要檢視區域被視訊佔據。 當未指定大小時，通常會設定為符合可用的裝置畫面。
seo-title: 主檢視器區域
solution: Experience Manager
title: 主檢視器區域
topic: Dynamic media
uuid: f395b22d-55b8-4422-9aa4-9dd4b7a24063
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 主檢視器區域{#main-viewer-area}

主要檢視區域被視訊佔據。 當未指定大小時，通常會設定為符合可用的裝置畫面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

下列CSS類別選取器會控制檢視區域的外觀：

```
.s7videoviewer 
```

## 主檢視器區域的CSS屬性 {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>檢視器寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>檢視器高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要設定具有白色背景(#FFFFFF)的視訊檢視器，並使其大小為512 x 288像素：

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

