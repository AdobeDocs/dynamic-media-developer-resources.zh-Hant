---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---

# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> 控制下拉面板外觀的方向。 </p> <p>當設定為<span class="codeph"> fit-vertical</span>時，元件首先將基板位置移動到按鈕的底部，並嘗試從基部位置向右或向左滾動面板。 每次嘗試時，元件都會檢查面板是否被外部容器修剪。 如果所有嘗試均失敗，則元件會嘗試將基板位置移至頂部，並在左右方向重複展開嘗試。 </p> <p>當設為<span class="codeph"> fit-lateral</span>時，元件使用類似的邏輯，但會先將底座向右移動，然後向下和向上滾動方向。 然後，它把基座向左移動，向下和向上展開。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 為下拉式自動隱藏計時器設定秒數的延遲，該計時器會在使用者閒置時隱藏面板。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-55436ddd78b04f538dbb9a7a8463feae}

選填。

## 預設 {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## 範例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
