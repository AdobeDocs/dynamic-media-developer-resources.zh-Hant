---
title: PanoramicView.fmt
description: 指定元件從「影像伺服器」載入影像時所用的影像格式。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

指定元件從「影像伺服器」載入影像時所用的影像格式。 如果指定的格式結尾為&quot;-alpha&quot;，元件會將影像呈現為透明。 至於所有其他影像格式，元件會將影像視為不透明。 元件預設為透明背景。 因此，若要使其不透明，請將`background-color` CSS屬性設定為`desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> 指定元件從「影像伺服器」載入影像時所用的影像格式。 如果指定的格式結尾為"-alpha"，元件會將影像呈現為透明內容，至於所有其他影像格式，元件會將影像視為不透明。 元件預設為透明背景。 因此，若要不透明，請將background-color CSS屬性設定為所要的顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
