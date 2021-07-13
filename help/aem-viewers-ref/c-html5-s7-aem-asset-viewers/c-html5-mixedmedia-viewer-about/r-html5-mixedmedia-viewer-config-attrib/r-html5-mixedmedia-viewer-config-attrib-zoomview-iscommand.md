---
description: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,User
exl-id: faa6344a-a0b5-4b27-818b-81e9e0b721b4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '66'
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

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

無。

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

在檢視器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在設定資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
