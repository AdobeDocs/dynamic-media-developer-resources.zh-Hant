---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`靈敏`*[, *`度`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制透過滑鼠拖曳或滑動所執行的水準和垂直回轉的敏感度。 </p> <p> <span class="codeph"> </span> xSensitivity設定當使用者將滑鼠從檢視的一側水準拖曳到另一側時，會進行多少個水準產品旋轉。例如，3表示使用者會看到一個完整拖曳手勢的3個完整旋轉。 </p> <p>同樣地，<span class="codeph"> ySensitivity</span>控制垂直自旋的靈敏度。 值1表示一個完全垂直拖曳或滑動會將檢視角度從最上方回轉平面變更為最下方（反之亦然）。 </p> <p>為<span class="codeph"> ySensitivity</span>設定負值會反轉垂直自旋的方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
