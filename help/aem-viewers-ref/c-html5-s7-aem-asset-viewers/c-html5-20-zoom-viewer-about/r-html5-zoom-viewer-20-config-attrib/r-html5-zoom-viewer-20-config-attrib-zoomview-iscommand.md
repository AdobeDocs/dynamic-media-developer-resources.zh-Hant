---
description: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,User
exl-id: bab0a648-a365-4df1-bded-ba0202e62e1f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> 應用於縮放影像的「影像伺服」命令字串。 如果在URL中指定，則所有<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的出現次數必須分別以<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>進行HTTP編碼。 </p> <p> <p>注意： 不支援影像大小調整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

無。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

在檢視器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在設定資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
