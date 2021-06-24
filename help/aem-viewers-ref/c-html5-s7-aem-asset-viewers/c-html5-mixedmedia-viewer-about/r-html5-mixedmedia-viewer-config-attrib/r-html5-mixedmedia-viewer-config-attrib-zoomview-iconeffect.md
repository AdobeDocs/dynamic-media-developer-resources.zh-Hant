---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 40b7887d-d525-4816-8c72-9ef8f5948de3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

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

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
