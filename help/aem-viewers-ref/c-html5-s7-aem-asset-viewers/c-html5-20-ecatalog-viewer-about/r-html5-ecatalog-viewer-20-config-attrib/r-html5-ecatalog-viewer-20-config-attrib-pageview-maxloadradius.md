---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic media
uuid: 425624c5-3cbe-4b63-8c6b-eff31f2ed919
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
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
   <td colname="col2"> <p>指定元件預載行為。 </p> <p>當設定為<span class="codeph"> -1</span>時，元件將在空閒狀態中預載所有目錄幀。 </p> <p> 當設定為<span class="codeph"> 0</span>時，元件僅載入當前可見的幀、前一個幀和下一個幀。 </p> <p>將<span class="codeph"><span class="varname"> preloadnbr</span></span>設為定義當前顯示幀周圍有多少不可見幀處於空閒狀態。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4b7952997f9240e581d21bcdb173f9af}

選填。

## 預設 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 範例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
