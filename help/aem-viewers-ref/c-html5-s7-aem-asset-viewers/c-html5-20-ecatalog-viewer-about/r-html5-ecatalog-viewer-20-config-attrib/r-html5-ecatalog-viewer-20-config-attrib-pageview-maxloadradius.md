---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件預先載入行為。 </p> <p>設定為<span class="codeph"> -1</span>時，元件會在閒置狀態中預先載入所有目錄框架。 </p> <p> 設定為<span class="codeph"> 0</span>時，元件僅載入目前可見的影格、上一個影格和下一個影格。 </p> <p>設定<span class="codeph"><span class="varname"> preloadnbr</span></span>以定義目前顯示影格周圍有多少隱藏影格在閒置狀態中預先載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4b7952997f9240e581d21bcdb173f9af}

選擇性.

## 預設 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 範例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
