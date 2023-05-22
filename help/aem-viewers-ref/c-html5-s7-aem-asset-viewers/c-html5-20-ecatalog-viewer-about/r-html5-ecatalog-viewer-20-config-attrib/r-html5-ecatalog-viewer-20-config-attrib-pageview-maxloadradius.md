---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`預載入br`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> 預載入br</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件預載入行為。 </p> <p>設定為時 <span class="codeph"> -1</span> 元件在空閒狀態下預載所有目錄幀。 </p> <p> 設定為時 <span class="codeph"> 0</span> 該元件僅載入當前可見的幀、上一幀和下一幀。 </p> <p>設定 <span class="codeph"><span class="varname"> 預載入br</span></span> 定義當前顯示的幀周圍以空閒狀態預載的不可見幀的數量。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4b7952997f9240e581d21bcdb173f9af}

選擇性.

## 預設 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 範例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
