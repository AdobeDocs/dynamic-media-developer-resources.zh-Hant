---
description: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
topic: Dynamic media
uuid: 76a2793e-bda0-408c-b09e-767a3ef27986
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>指定元件用於從Image Server載入映像的映像格式。 如果指定的格式以<span class="codeph"> -alpha</span>結尾，則元件會將影像渲染為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 請注意，元件預設有白色背景。 因此，要使背景透明化，請將<span class="codeph"> background-color</span> CSS屬性設為<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt-png-alpha`
