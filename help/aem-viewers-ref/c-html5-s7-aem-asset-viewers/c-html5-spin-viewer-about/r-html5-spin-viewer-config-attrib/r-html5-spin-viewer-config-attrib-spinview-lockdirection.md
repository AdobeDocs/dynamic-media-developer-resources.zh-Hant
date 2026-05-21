---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
TQID: 'https://experienceleague.adobe.com/eTB-wD8G7HGSDgohQn-FsCeFL1GHMBiqzNUtT3nw5n4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 指定如果有2D迴轉集，是否允許變更迴轉方向。 </p> <p>設定為<span class="codeph"> 1 </span>時，元件會在手勢開頭識別主要拖曳或撥動方向（水平與垂直）。 之後，它會維持該方向直到該手勢結束。 例如，如果使用者開始水準迴轉，然後決定沿垂直方向繼續拖曳手勢，則元件不會執行垂直迴轉。 而是隻考慮滑鼠或撥動的水準移動。 </p> <p>值為<span class="codeph"> 0 </span>可讓使用者在手勢進度期間隨時變更迴轉方向。 如果迴轉集是1D，此設定就沒有作用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
