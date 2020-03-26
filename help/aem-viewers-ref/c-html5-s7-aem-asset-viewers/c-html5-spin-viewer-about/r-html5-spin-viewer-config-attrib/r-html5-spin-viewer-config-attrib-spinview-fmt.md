---
description: 'null'
seo-description: 'null'
seo-title: SpinView.fmt
solution: Experience Manager
title: SpinView.fmt
topic: Dynamic media
uuid: 6004d8ab-7dc7-451d-b0e2-4f6d308203d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從Image Server載入映像的映像格式。 如果指定的格式以 <span class="codeph"> -alpha結尾</span>，則元件會將影像渲染為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 依預設，元件具有白色背景。 因此，若要將它設為透明，請 <span class="codeph"> 將背景顏色</span> CSS屬性設 <span class="codeph"> 為透明</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`jpeg`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`fmt=png-alpha`
