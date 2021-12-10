---
title: ZoomView.fmt
description: ZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b46daa2f-d565-4502-8842-2b95303a77d2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從影像伺服器載入影像的影像格式。 如果指定的格式結尾為 <span class="codeph"> -α</span>，元件會將影像轉譯為透明內容。 對於所有其他影像格式，元件將影像視為不透明。 依預設，元件有白色背景。 因此，若要使其透明，請將 <span class="codeph"> 背景顏色</span> CSS屬性 <span class="codeph"> 透明</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
