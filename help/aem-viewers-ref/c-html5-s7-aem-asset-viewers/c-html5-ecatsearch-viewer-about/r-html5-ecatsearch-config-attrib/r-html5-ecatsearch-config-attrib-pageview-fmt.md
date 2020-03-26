---
description: 'null'
seo-description: 'null'
seo-title: PageView.fmt
solution: Experience Manager
title: PageView.fmt
topic: Dynamic media
uuid: bbae406c-9169-4944-8e91-f2d7c8011520
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.fmt{#pageview-fmt}

[!DNL `[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從Image Server載入映像的映像格式。 如果指定的格式以 <span class="codeph"> -alpha結尾</span>，則元件會將影像渲染為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 依預設，元件具有白色背景。 因此，若要將它設為透明，請 <span class="codeph"> 將背景顏色</span> CSS屬性設 <span class="codeph"> 為透明</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

選填。

## 預設 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## 範例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
