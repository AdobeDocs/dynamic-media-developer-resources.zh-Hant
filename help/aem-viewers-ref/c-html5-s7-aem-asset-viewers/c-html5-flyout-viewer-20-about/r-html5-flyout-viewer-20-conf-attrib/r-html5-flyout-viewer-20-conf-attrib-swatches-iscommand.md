---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: ed587082-3306-4914-916f-db37a823e199
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 應用於所有色板的「影像伺服」命令字串。 若已在URL中指定，請務必將 <span class="codeph"> &amp;</span> 和 <span class="codeph"> =</span> as <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>，分別為。 </p> <p> <p>注意：不支援影像大小調整操作命令。 </p> </p> </td> 
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
