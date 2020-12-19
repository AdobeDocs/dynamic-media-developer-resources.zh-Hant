---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: InteractiveSwatches.fmt
solution: Experience Manager
title: InteractiveSwatches.fmt
topic: Dynamic media
uuid: 0a30c913-39d1-4521-b65c-f2b3879f6928
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---


# InteractiveSwatches.fmt{#interactiveswatches-fmt}

互動式視訊檢視器的設定屬性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從Image Server載入映像的映像格式。 </p> <p>如果指定的格式以"<span class="codeph"> -alpha</span>"結尾，元件會將影像呈現為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 請注意，元件預設有白色背景。 因此，要使其完全透明，請將<span class="codeph"> background-color</span> CSS屬性設為<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```

