---
description: 當目前資產是回轉集時，主檢視會由回轉影像組成。
seo-description: 當目前資產是回轉集時，主檢視會由回轉影像組成。
seo-title: 回轉視圖
solution: Experience Manager
title: 回轉視圖
topic: Dynamic media
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Spin view{#spin-view}

當目前資產是回轉集時，主檢視會由回轉影像組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

檢視區域的外觀會使用下列CSS類別選擇器加以控制：

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 回轉視圖的十六進位格式背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——使回轉視圖透明。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

