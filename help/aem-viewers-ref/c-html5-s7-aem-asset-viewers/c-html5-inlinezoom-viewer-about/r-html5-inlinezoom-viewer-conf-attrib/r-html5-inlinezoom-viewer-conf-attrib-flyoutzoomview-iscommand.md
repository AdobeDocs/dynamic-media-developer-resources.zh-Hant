---
description: FlyoutZoomView.iscommand
solution: Experience Manager
title: FlyoutZoomView.iscommand
feature: Dynamic Media Classic，檢視器，SDK/API，內嵌縮放
role: Developer,User
exl-id: 2ae17dc8-2728-4ee5-ba88-45d78a0f4d9a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>應用於FlyoutZoomView主影像和在視圖中縮放的「影像伺服」命令字串。 如果已在URL中指定，請務必將<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有出現次數分別以<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>編碼。 </p> <p> <p>注意： 不支援影像大小調整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

無。

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

在檢視器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
