---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: b5b0acab-4e11-4f6a-8cb1-be6d683d7384
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`是命令`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 是命令</span> </span> </p> </td> 
   <td colname="col2"> <p> 應用於所有色板的「影像服務」命令字串。 如果在URL中指定，請確保HTTP編碼所有出現的 <span class="codeph"> &amp;</span> 和 <span class="codeph"> =</span> 如 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>的下界。 </p> <p> <p>注：不支援影像大小調整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選擇性.

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

無。

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

在查看器URL中指定時。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置資料中指定時。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
