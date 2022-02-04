---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定是否允許在存在2D旋轉集時改變旋轉方向。 </p> <p>設定為時 <span class="codeph"> 1 </span>，該元件在手勢的開始處標識主拖動方向或滑動方向（水準方向與垂直方向）。 之後，它會保持這個方向直到手勢結束。 例如，如果用戶開始水準旋轉，然後決定在垂直方向上繼續拖動手勢，則元件不執行垂直旋轉。 相反，它只考慮滑鼠或滑動的水準移動。 </p> <p>值 <span class="codeph"> 0 </span> 允許用戶在手勢處理過程中隨時更改旋轉方向。 如果旋轉集為1D，則設定無效。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
