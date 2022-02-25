---
title: ZoomView.iscommand
description: ZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d1f54ef2-4ed4-4fb6-9913-98bf194f9afc
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`是命令`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> iscommand（iscommand命令）</span> </span> </p> </td> 
   <td colname="col2"> <p> 用於縮放影像的「影像服務」命令字串。 如果在URL中指定，則 <span class="codeph"> &amp;</span> 和 <span class="codeph"> =</span> 必須是HTTP編碼為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>的下界。 </p> <p> <p>注：不支援影像大小調整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

無。

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

在查看器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
