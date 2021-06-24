---
description: SpinView.iconeffect
solution: Experience Manager
title: SpinView.iconeffect
feature: Dynamic Media Classic，檢視器，SDK/API，回轉集
role: Developer,Business Practitioner
exl-id: e84336da-7f33-4fa9-b881-93b9db4bae8b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 使<span class="codeph"> iconeffect</span>在影像處於重置狀態時顯示在影像的頂部，並且它暗示了可用的操作以與影像交互。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定<span class="codeph"> iconeffect</span>出現並重新出現的次數上限。 值<span class="codeph"> -1</span>表示圖示一律會無限期重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 淡出</span></span> </p> </td> 
   <td colname="col2"> <p>指定顯示或隱藏動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>設定<span class="codeph"> iconeffect</span>在自動隱藏前保持完全可見的秒數。 即，淡出動畫完成之後、淡出動畫開始之前的時間。 <span class="codeph"> 0</span>的設定禁用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`
