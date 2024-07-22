---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 2%

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
