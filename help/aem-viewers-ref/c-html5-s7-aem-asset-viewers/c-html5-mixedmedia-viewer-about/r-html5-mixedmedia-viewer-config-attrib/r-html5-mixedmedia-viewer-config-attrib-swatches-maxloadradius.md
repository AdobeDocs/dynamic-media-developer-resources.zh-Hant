---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 06f493d7-18c9-4bb1-add6-a0dfd1a689bd
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>指定元件預載行為。 當設為<span class="codeph"> -1</span>時，初始化元件或變更資產時，會同時載入所有色票。 </p> <p>設為<span class="codeph"> 0</span>時，只會載入可見色票。 </p> <p><span class="codeph"><span class="varname"> </span></span> preloadnbr定義了預載入可見區域周圍的不可見行/列的數量。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
