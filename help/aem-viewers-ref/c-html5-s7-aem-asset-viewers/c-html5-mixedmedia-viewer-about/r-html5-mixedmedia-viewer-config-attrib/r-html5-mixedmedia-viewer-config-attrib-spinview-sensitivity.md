---
title: SpinView.sensibility
description: SpinView.sensibility
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
TQID: 'https://experienceleague.adobe.com/xRqLAbFehJYLGgevPmISxILSWWyedyBSDkbNZTDs808'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# SpinView.sensibility{#spinview-sensitivity}

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
