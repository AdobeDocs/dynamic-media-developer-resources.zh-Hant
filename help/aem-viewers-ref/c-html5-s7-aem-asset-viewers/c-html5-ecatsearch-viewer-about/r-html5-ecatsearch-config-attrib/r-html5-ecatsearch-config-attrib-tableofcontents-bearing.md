---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`自動隱藏延遲`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 擬合橫向|擬合垂直</span> </p> </td> 
   <td> <p> 控制下拉面板外觀的方向。 </p> <p>設定為時 <span class="codeph"> 垂直</span>，元件首先將基板位置移到其按鈕的底部，並嘗試從基板位置向右或向左滾動面板。 每次嘗試時，元件都會檢查面板是否被外部容器夾住。 如果所有嘗試都失敗，則元件將嘗試將基板位置移到頂部，並重複沿左右方向展開嘗試。 </p> <p>設定為時 <span class="codeph"> 擬合側</span>，該元件使用相似的邏輯，但首先將基本向右移動，然後嘗試向下和向上展開。 然後，它把底座向左移動，試圖上下滾動方向。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 自動隱藏延遲</span></span> </p> </td> 
   <td> <p> 設定下拉清單自動隱藏計時器的延遲（秒），該計時器在用戶空閒時隱藏面板。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-55436ddd78b04f538dbb9a7a8463feae}

選擇性.

## 預設 {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## 範例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
