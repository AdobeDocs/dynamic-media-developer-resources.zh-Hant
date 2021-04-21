---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---


# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 套用至所有縮圖的「影像伺服」命令字串。 如果在URL中指定，所有<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的出現次數都必須分別以HTTP編碼為<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-df5a0604766b4ac2b9a6742b377e427c}

選填。

## 預設 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

無。

## 範例 {#section-813de2905d6c44c0991cfe0931581462}

在檢視器URL中指定時。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

在配置資料中指定時。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
