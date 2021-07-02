---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 3336c4d2-0d1d-4c6f-8163-8a84a8be8c20
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 應用於所有色板的「影像伺服」命令字串。 如果已在URL中指定，請務必將<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有出現次數分別以<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>編碼。 </p> <p> <p>注意： 不支援影像大小調整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

無。

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

在檢視器URL中指定時。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置資料中指定時。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
