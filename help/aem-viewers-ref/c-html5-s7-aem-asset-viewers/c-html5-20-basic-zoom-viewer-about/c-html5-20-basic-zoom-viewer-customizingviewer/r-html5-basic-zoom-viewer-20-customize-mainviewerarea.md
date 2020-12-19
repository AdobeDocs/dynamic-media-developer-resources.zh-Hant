---
description: 主視圖區域是縮放影像所佔用的區域。 當未指定大小時，通常會設定為符合可用的裝置畫面。
seo-description: 主視圖區域是縮放影像所佔用的區域。 當未指定大小時，通常會設定為符合可用的裝置畫面。
seo-title: 主檢視器區域
solution: Experience Manager
title: 主檢視器區域
topic: Dynamic media
uuid: f37b8d25-4bd6-481e-88e7-98192186b177
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---


# 主檢視器區域{#main-viewer-area}

主視圖區域是縮放影像所佔用的區域。 當未指定大小時，通常會設定為符合可用的裝置畫面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

檢視區域的外觀會使用下列CSS類別選擇器加以控制：

```
.s7basiczoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p> 十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——設定具有白色背景(`#FFFFFF`)的檢視器，並使其大小為512 x 288像素。

```
.s7basiczoomviewer{ 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

