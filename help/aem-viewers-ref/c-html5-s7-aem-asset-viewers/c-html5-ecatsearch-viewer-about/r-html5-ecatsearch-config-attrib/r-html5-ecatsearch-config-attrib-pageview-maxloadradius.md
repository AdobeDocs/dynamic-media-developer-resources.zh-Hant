---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
uuid: e60603a5-06dc-43e3-a380-b4d97fc539f1
feature: Dynamic Media經典，檢視器，SDK/API,eCatalog搜尋
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---


# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

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

[!DNL `1`]

## 範例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
