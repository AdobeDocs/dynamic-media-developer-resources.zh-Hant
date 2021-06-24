---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: c2bbcb99-eeef-4793-a132-d0bd1fefb534
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件預載行為。 </p> <p>當設為<span class="codeph"> -1</span>時，當元件初始化或資產變更時，所有縮圖會同時載入。 </p> <p> 設為<span class="codeph"> 0</span>時，只會載入可見的縮圖。 </p> <p>設定<span class="codeph"><span class="varname"> preloadnbr</span></span>以定義預載入的可見區域周圍的不可見行數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4b7952997f9240e581d21bcdb173f9af}

選填。

## 預設 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 範例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
