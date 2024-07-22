---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 574cb37c-009a-43c7-ae55-8b26c0c096c5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 5%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定元件預先載入行為。 當設定為<span class="codeph"> -1</span>時，當初始化元件或變更資產時，所有色票都會同時載入。 設定為<span class="codeph"> 0</span>時，只會載入可見的色票。 </p> <p><span class="codeph"> <span class="varname"> preloadnbr</span></span>定義可見區域周圍預先載入的隱藏列/欄數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選擇性.

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`
