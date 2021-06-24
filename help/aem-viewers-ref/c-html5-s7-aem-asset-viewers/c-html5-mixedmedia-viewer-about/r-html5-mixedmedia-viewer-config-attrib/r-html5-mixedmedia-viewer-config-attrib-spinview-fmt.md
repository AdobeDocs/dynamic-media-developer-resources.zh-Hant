---
description: SpinView.fmt
solution: Experience Manager
title: SpinView.fmt
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 4bb6c242-9f1a-440f-9fca-bf26e66e4114
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 4%

---

# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_68C0C3D5C60640DC9A8EE04EA685AB99"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從影像伺服器載入影像的影像格式。 如果指定的格式結尾為<span class="codeph"> -alpha</span>，則元件會將影像呈現為透明內容。 對於所有其他影像格式，元件將影像視為不透明。 </p> <p>依預設，元件有白色背景。 因此，若要使其透明，請將<span class="codeph"> background-color</span> CSS屬性設定為<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
