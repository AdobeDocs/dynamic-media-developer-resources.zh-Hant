---
title: PageView.fmt
description: PageView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 07aec907-fb9d-41c8-9f32-a4886605db35
source-git-commit: 5432393e265fba888579d700cf2f414dc4f680af
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件從「影像伺服器」載入影像時所用的影像格式。 如果指定的格式結尾為<span class="codeph"> -alpha</span>，元件會將影像呈現為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 元件預設為白色背景。 因此，若要使其透明，請將<span class="codeph"> background-color</span> CSS屬性設定為<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

選擇性.

## 預設 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## 範例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
