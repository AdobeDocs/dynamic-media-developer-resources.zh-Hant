---
title: InteractiveSwatches.fmt
description: Interactive Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9a751b91-aeff-4ee1-b2fe-9bec416884ab
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Interactive Video Viewer的配置屬性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從Image Server載入影像的影像格式。 </p> <p>如果指定的格式以"結尾<span class="codeph"> -α</span>」，該元件將影像渲染為透明內容。 對於所有其它影像格式，元件將影像視為不透明。 預設情況下，該元件具有白色背景。 因此，要使其透明化， <span class="codeph"> 背景色</span> CSS屬性到 <span class="codeph"> 透明</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```
