---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 3%

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定在2D回轉集的情況下是否允許回轉方向改變。 </p> <p>當設為<span class="codeph"> 1 </span>時，元件會在手勢開始時識別主要拖曳或滑動方向（水準與垂直）。 之後，它會維持該方向，直到手勢結束。 例如，如果使用者啟動水準旋轉，然後決定繼續在垂直方向拖曳手勢，則元件不會執行垂直旋轉；而是只考慮滑鼠或滑動的水準移動。 </p> <p>值<span class="codeph"> 0 </span>可讓使用者在手勢進行期間隨時變更回轉方向。 如果回轉集為1D，則設定不會影響。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
