---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件預先載入行為。 </p> <p>設定為<span class="codeph"> -1</span>時，元件會在閒置狀態中預先載入所有目錄框架。 </p> <p> 設定為<span class="codeph"> 0</span>時，元件僅載入可見的影格、上一個影格和下一個影格。 </p> <p>設定<span class="codeph"><span class="varname"> preloadnbr</span></span>以定義目前顯示影格周圍有多少隱藏影格在閒置狀態中預先載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4b7952997f9240e581d21bcdb173f9af}

選擇性.

## 預設 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 範例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
