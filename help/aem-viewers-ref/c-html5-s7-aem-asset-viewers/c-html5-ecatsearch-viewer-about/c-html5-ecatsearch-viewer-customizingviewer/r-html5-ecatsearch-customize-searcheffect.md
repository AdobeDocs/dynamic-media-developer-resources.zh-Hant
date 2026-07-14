---
title: 搜尋效果
description: 檢視器會在主檢視中顯示搜尋結果區域，以反白顯示目錄中的文字或片語。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
TQID: 'https://experienceleague.adobe.com/h30DfEeB69i1gbnfOvnKphglRkXgcvOTG8L-eTZv2GU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 1%

---

# 搜尋效果{#search-effect}

檢視器會在主檢視中顯示搜尋結果區域，以反白顯示目錄中的文字或片語。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主要檢視器區域的&#x200B;**CSS屬性**

搜尋結果區域的外觀由下列CSS類別選取器控制：

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景</span> </p> </td> 
   <td colname="col2"> <p>搜尋結果區域的背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定具有半透明、黃色填色的搜尋結果區域：

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

