---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
topic: Dynamic media
uuid: b4512555-edab-4818-86c0-e224775ecb2c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---


# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從Image Server載入映像的映像格式。 如果指定的格式以<span class="codeph"> -alpha</span>結尾，則元件會將影像渲染為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 依預設，元件具有白色背景。 因此，若要將其設為透明，請將<span class="codeph"> background-color</span> CSS屬性設為<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
