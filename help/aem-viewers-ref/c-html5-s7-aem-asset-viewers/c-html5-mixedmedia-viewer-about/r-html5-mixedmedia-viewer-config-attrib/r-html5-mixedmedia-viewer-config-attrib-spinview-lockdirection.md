---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,User
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定在2D回轉集的情況下是否允許回轉方向改變。 </p> <p>當設為<span class="codeph"> 1 </span>時，元件會在手勢開始時識別主要的拖曳或滑動方向（水準與垂直）。 之後，它會維持該方向，直到手勢結束為止。 例如，如果用戶啟動水準回轉，然後決定沿垂直方向繼續拖曳手勢，則元件不會執行垂直回轉；相反，它只考慮滑鼠或滑動的水準移動。 </p> <p>值<span class="codeph"> 0 </span>可讓使用者在手勢進行期間隨時變更回轉方向。 如果回轉集為1D，則設定不會影響。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
