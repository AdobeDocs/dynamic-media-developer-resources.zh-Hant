---
description: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
topic: Dynamic media
uuid: 0befdc0b-dd58-4aae-90e6-8c578f3b6c6f
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---


# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> iscommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 套用至縮放影像的「影像伺服」命令字串。 如果在URL中指定，所有<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的出現次數都必須分別以HTTP編碼為<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>。 </p> <p> <p>注意： 不支援影像大小調整指令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

無。

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

在檢視器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
