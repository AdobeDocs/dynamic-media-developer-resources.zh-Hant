---
description: 指定元件用於從影像伺服器載入影像的影像格式。
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

指定元件用於從影像伺服器載入影像的影像格式。

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td colname="col2"> <p> 如果指定的格式結尾為<span class="codeph"> -alpha</span>，則元件會將影像呈現為透明內容。 對於所有其他影像格式，元件將影像視為不透明。 </p> <p>請注意，元件預設為白色背景。 因此，要使其完全透明，請將<span class="codeph"> background-color</span> CSS屬性設定為<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
