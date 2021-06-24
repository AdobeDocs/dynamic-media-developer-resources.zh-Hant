---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 指定提示文本在隱藏之前顯示的秒數。 當設定為<span class="codeph"> -1</span>時，即使用戶激活彈出，仍始終顯示消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定檢視集合中的新影像時顯示文字的次數。 值<span class="codeph"> -1</span>表示在檢視集合中的任何影像時，一律會顯示文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 淡出</span></span> </p> </td> 
   <td colname="col2"> 指定文本出現或消失時出現的淡化動畫的持續時間。 值<span class="codeph"> 0</span>表示沒有淡出轉變。 </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
