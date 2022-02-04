---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`x敏感度`*[, *`敏感度`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> x敏感度</span>[, <span class="varname"> 敏感度</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制用滑鼠拖動或滑動執行的水準和垂直旋轉的敏感度。 </p> <p> <span class="codeph"> x敏感度</span> 設定如果用戶將滑鼠從視圖的一側水準拖動到另一側，則執行多少次完全水準產品旋轉。 例如，三表示用戶看到一個完全拖動手勢的三個完全旋轉。 </p> <p>同樣， <span class="codeph"> 敏感度</span> 控制垂直旋轉的靈敏度。 值1表示一個完全垂直的拖動或滑動會將視圖角度從最頂部旋轉平面更改為最底部（或相反）。 </p> <p>設定負值 <span class="codeph"> 敏感度</span> 反轉垂直旋轉的方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
