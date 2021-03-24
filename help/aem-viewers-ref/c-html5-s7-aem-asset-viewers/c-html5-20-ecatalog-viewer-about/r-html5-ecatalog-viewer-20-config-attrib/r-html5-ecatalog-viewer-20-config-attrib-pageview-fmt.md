---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
feature: Dynamic Media經典，檢視器，SDK/API,eCatalog
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---


# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從Image Server載入映像的映像格式。 如果指定的格式以<span class="codeph"> -alpha</span>結尾，則元件會將影像渲染為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 依預設，元件具有白色背景。 因此，若要將其設為透明，請將<span class="codeph"> background-color</span> CSS屬性設為<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

選填。

## 預設 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## 範例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
