---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 2%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> 控制下拉面板外觀的方向。 </p> <p>設為時 <span class="codeph"> 垂直擬合</span>，元件會先將基板位置移至按鈕底部，並嘗試從基底位置向右或向左卷出面板。 每次嘗試時，元件都會檢查面板是否被外部容器修剪。 如果所有嘗試失敗，元件會嘗試將基板位置移至頂端，然後在左右方向重複轉出嘗試。 </p> <p>設為時 <span class="codeph"> 側向擬合</span>，元件會使用類似的邏輯，但會先將底部向右移動，然後嘗試向下和向上移動方向。 然後，它把底座向左移動，向下和向上移動。 </p> </td> 
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

`fit-vertical,2`

## 範例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
