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
ht-degree: 6%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件預載行為。 </p> <p>設為時 <span class="codeph"> -1</span> 當處於空閒狀態時，元件將預載入所有目錄幀。 </p> <p> 設為時 <span class="codeph"> 0</span> 元件僅載入當前可見、前一幀和下一幀的幀。 </p> <p>設定 <span class="codeph"><span class="varname"> preloadnbr</span></span> 定義當前顯示的幀周圍的不可見幀數，這些幀預載入為空閒狀態。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4b7952997f9240e581d21bcdb173f9af}

選填。

## 預設 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 範例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
