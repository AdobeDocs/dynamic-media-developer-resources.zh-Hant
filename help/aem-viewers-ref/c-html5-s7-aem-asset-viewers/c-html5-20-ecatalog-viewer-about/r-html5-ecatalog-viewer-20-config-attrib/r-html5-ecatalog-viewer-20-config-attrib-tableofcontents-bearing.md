---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
topic: Dynamic media
uuid: 791aaaa5-3777-4f68-a445-caa3d975d883
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> 控制下拉式面板外觀的方向。 </p> <p>當設為<span class="codeph"> fit-vertical</span>時，元件會先將底板位置移至按鈕底部，並嘗試從底部位置向右或向左捲動面板。 每次嘗試時，元件都會檢查面板是否被外部容器剪裁。 如果所有嘗試都失敗，元件會嘗試將基板位置移至頂端，並在左右方向重複推出嘗試。 </p> <p>當設為<span class="codeph"> fit-lateral</span>時，元件使用類似的邏輯，但會先將基座向右移動，嘗試向下和向上展開方向。 然後，它把底座向左移動，向下和向上展開。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 設定下拉式自動隱藏計時器的延遲（以秒為單位），當使用者閒置時，此計時器會隱藏面板。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-55436ddd78b04f538dbb9a7a8463feae}

選填。

## 預設 {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## 範例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
