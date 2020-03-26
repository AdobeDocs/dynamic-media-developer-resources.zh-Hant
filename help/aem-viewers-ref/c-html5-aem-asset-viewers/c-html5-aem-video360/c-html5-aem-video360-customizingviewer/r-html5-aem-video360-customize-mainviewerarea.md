---
description: 主要檢視區域是360視訊所佔用的區域。 當未指定大小時，通常會將它設為符合可用的裝置畫面。
seo-description: 主要檢視區域是360視訊所佔用的區域。 當未指定大小時，通常會將它設為符合可用的裝置畫面。
seo-title: 主檢視器區域
solution: Experience Manager
title: 主檢視器區域
topic: Dynamic media
uuid: ec321901-f077-4f71-a48c-20cae11c41d1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 主檢視器區域{#main-viewer-area}

主要檢視區域是360視訊所佔用的區域。 當未指定大小時，通常會將它設為符合可用的裝置畫面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

檢視區域的外觀會使用下列CSS類別選擇器加以控制：

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
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-ee18025b182a42dc98052de5f133ddfe}

若要設定具有白色背景( `#FFFFFF`)的檢視器，並將其大小設為512 x 288像素。

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

