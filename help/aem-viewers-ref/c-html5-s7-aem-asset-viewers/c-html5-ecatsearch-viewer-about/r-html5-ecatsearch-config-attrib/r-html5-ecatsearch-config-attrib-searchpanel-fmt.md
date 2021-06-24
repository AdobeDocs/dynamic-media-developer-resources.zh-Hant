---
description: SearchPanel.fmt
solution: Experience Manager
title: SearchPanel.fmt
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: a713b8f1-e834-457d-b038-eb30b25f905f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# SearchPanel.fmt{#searchpanel-fmt}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從影像伺服器載入影像的影像格式。 影像伺服器和用戶端瀏覽器可支援任何格式。 </p> <p>如果指定的格式結尾為<span class="codeph"> -alpha</span>，則元件會將影像呈現為透明內容。 對於所有其他影像格式，元件將影像視為不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

選填。

## 預設 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## 範例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
