---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: fd1fa0f2-d666-4470-8b5b-673f3c4327e0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---

# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 套用至頁面影像的「影像伺服」命令字串。 如果在URL中指定，則所有<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的出現次數必須分別以<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>進行HTTP編碼。 </p> <p> <p>注意： 不支援影像大小調整操作命令。 </p> </p> </td> 
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

在設定資料中指定時。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
