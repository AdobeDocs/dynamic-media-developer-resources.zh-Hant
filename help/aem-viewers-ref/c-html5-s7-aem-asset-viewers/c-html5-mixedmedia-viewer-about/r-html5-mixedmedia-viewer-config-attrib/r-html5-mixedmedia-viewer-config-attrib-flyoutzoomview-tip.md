---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 6%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持續時間`*[, *`計數`*][, *`淡`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 指定提示文本隱藏之前顯示的秒數。 設定為時 <span class="codeph"> -1</span>，即使用戶激活彈出窗口，消息也始終顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定查看集合中的新影像時顯示文本的次數。 值 <span class="codeph"> -1</span> 表示在查看集中的任何影像時始終顯示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 淡</span></span> </p> </td> 
   <td colname="col2"> 指定當文本出現或消失時出現的淡入動畫的持續時間。 值 <span class="codeph"> 0</span> 指示無淡入色過渡。 </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
