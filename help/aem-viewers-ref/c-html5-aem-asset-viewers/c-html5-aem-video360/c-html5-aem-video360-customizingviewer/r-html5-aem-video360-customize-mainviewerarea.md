---
description: 主要的觀看區域是360視頻所佔用的區域。 當未指定大小時，通常會設定為適合可用的裝置畫面。
solution: Experience Manager
title: 主觀看者區域
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,User
exl-id: 912cb4b3-6409-48ed-9b9c-968b63718a1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 主觀看者區域{#main-viewer-area}

主要的觀看區域是360視頻所佔用的區域。 當未指定大小時，通常會設定為適合可用的裝置畫面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

查看區域的外觀由以下CSS類選擇器控制：

```
.s7video360viewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>檢視器的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>檢視器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 以十六進位格式表示的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-ee18025b182a42dc98052de5f133ddfe}

設定具有白色背景的檢視器(`#FFFFFF`)，並使其大小為512 x 288像素。

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
