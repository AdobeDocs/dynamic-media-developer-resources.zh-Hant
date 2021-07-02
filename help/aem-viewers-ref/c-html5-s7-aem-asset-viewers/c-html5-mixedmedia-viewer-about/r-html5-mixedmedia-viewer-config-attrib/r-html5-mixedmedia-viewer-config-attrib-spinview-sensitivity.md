---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivitySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> x敏感</span>[,  <span class="varname"> y敏感</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制滑鼠拖動或滑動時執行的水準和垂直回轉的靈敏度。 </p> <p> <span class="codeph"> </span> x敏感度設定如果使用者將滑鼠從檢視的一側水準拖曳到另一側，會執行多少次完全水準的產品旋轉。例如，三表示使用者會看到一個完整拖曳手勢的三個完整旋轉。 </p> <p>同樣，<span class="codeph"> ySensitivity</span>控制垂直自旋的靈敏度。 如果值為1，表示一個垂直的完全拖動或滑動會將視圖角度從最上方的旋轉平面更改為最下方（反之亦然）。 </p> <p>為<span class="codeph"> ySensitivity</span>設定負值會反轉垂直自旋的方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
