---
description: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,User
exl-id: 043196c8-63ab-439e-a28f-b76d1467f26e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td> <p>指定元件用於從影像伺服器載入影像的影像格式。 如果指定的格式結尾為<span class="codeph"> -alpha</span>，則元件會將影像呈現為透明內容。 對於所有其他影像格式，元件將影像視為不透明。 請注意，元件預設為白色背景。 因此，要使背景透明化，請將<span class="codeph"> background-color</span> CSS屬性設定為<span class="codeph">透明</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt-png-alpha`
