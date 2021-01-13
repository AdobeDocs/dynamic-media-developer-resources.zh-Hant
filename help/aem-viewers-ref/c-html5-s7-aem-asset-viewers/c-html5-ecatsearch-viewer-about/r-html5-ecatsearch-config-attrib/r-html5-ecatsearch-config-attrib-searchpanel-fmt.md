---
description: SearchPanel.fmt
solution: Experience Manager
title: SearchPanel.fmt
topic: Dynamic media
uuid: 58b88cc9-e07a-47aa-a0d2-c81428ca4d1e
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---


# SearchPanel.fmt{#searchpanel-fmt}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從Image Server載入映像的映像格式。 它可以是Image Server和用戶端瀏覽器支援的任何格式。 </p> <p>如果指定的格式以<span class="codeph"> -alpha</span>結尾，則元件會將影像渲染為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

選填。

## 預設 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## 範例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
