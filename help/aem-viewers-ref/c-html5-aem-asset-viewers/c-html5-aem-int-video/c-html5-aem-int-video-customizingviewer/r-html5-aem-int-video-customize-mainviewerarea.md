---
title: 主觀看者區域
description: 主視圖區域是交互色板所佔的區域。 若未指定大小，則此量度會設定為適合可用裝置畫面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 8e5a44fa-422f-46f3-bd85-86bd2ce03899
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 主觀看者區域{#main-viewer-area}

主視圖區域是交互色板所佔的區域。 若未指定大小，則此量度會設定為適合可用裝置畫面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

查看區域的外觀由以下CSS類選擇器控制：

```
.s7interactivevideoviewer
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
.s7interactivevideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
