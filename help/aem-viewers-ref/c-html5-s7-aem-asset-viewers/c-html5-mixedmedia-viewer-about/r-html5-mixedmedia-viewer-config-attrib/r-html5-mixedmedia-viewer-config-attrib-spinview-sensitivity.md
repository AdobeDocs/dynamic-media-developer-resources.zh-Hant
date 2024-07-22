---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`x敏感度`*[, *`y敏感度`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[， <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制以滑鼠拖曳或撥動方式執行的水平與垂直迴轉的靈敏度。 </p> <p> <span class="codeph"> xSensitivity</span>設定當使用者將滑鼠從檢視的一側水準拖曳到另一側時，產品會旋轉多少個水準。 例如，三個表示使用者看到一個完整拖曳手勢的三個完整旋轉。 </p> <p>同樣地，<span class="codeph"> ySensitivity</span>控制垂直迴轉的敏感度。 值為1表示一個完整的垂直拖曳或撥動會將檢視角度從最上層的迴轉平面變更為最下層（反之亦然）。 </p> <p>設定<span class="codeph"> ySensitivity</span>的負值會反轉垂直迴轉的方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
