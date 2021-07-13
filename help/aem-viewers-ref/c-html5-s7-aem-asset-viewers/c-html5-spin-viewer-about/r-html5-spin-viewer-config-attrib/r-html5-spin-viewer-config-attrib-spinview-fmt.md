---
description: SpinView.fmt
solution: Experience Manager
title: SpinView.fmt
feature: Dynamic Media Classic，檢視器，SDK/API，回轉集
role: Developer,User
exl-id: 3927d626-db16-4d30-80d3-5f63c3e9a110
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 5%

---

# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從影像伺服器載入影像的影像格式。 如果指定的格式結尾為<span class="codeph"> -alpha</span>，則元件會將影像呈現為透明內容。 對於所有其他影像格式，元件將影像視為不透明。 依預設，元件有白色背景。 因此，若要使其透明，請將<span class="codeph"> background-color</span> CSS屬性設定為<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`jpeg`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`fmt=png-alpha`
