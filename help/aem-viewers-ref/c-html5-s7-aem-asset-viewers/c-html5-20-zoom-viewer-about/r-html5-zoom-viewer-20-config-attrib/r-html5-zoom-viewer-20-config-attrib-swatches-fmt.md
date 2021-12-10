---
title: Swatches.fmt
description: Swatches.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8b47839a-ef3b-45ae-8e8d-5c9391d71d44
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td> <p>指定元件用於從影像伺服器載入影像的影像格式。 如果指定的格式結尾為 <span class="codeph"> -α</span>，元件會將影像轉譯為透明內容。 對於所有其他影像格式，元件將影像視為不透明。 依預設，元件有白色背景。 因此，要使背景透明化設定 <span class="codeph"> 背景顏色</span> CSS屬性 <span class="codeph"> 透明</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha`
