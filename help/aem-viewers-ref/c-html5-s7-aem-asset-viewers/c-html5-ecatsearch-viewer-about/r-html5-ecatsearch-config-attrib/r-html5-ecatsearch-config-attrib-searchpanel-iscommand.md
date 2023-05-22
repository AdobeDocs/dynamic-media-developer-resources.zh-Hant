---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 8%

---

# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`是命令`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 是命令</span></span> </p> </td> 
   <td colname="col2"> <p> 應用於所有縮略圖的「影像服務」命令字串。 如果在URL中指定，則 <span class="codeph"> &amp;</span> 和 <span class="codeph"> =</span> 必須是HTTP編碼為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>的下界。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-df5a0604766b4ac2b9a6742b377e427c}

選擇性.

## 預設 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

無。

## 範例 {#section-813de2905d6c44c0991cfe0931581462}

在查看器URL中指定時。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

在配置資料中指定時。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
