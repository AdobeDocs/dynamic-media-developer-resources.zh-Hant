---
title: 主觀看者區域
description: 主視區被智慧型裁切視頻佔據。 通常在未指定大小時設定為適合可用的裝置畫面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# 主觀看者區域{#main-viewer-area}

主觀區域被視頻佔據。 通常在未指定大小時設定為適合可用的裝置畫面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

以下CSS類選擇器控制查看區域的外觀：

```
.s7smartcropvideoviewer 
```

## 主查看器區域的CSS屬性 {#css-properties-of-the-main-viewer-area}

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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色 </span> </p> </td> 
   <td colname="col2"> <p> 以十六進位格式表示的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要設定白色背景的智慧型裁切視訊檢視器(#FFFFFF)，並將其大小設為512 x 288像素：

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
