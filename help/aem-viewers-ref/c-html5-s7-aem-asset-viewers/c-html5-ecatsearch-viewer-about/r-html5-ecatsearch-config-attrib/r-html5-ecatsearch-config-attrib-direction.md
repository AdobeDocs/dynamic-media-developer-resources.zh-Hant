---
title: 方向
description: 方向
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---

# 方向{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|靠左|靠右</span> </p> </td> 
   <td colname="col2"> <p>指定頁面在主檢視和縮圖中的顯示方式。 它也會指定使用者與檢視器使用者介面的互動方式，以在目錄框架之間變更。 </p> <p>使用<span class="codeph">左側</span>時，它會設定初始頁面的右對齊方式，以及最後一頁的左對齊方式。 它會以由左至右的呈現順序來拼接個別頁面子影像。 它也會設定主檢視，以使用由右至左的投影片動畫來推進目錄（如果<span class="codeph"> PageView.frametransition </span>設定為投影片）。 最後，縮圖會設定為由左至右的填入順序。 </p> <p>同樣地，使用<span class="codeph">右</span>時，它會設定初始頁面的左對齊方式，以及最後一頁的右對齊方式。 它會以由右至左的轉譯順序來拼接個別頁面子影像。 它也會設定主檢視，以使用由左至右的投影片動畫來推進目錄（如果<span class="codeph"> PageView.frametransition </span>設定為投影片）。 最後，這會反轉縮圖順序，讓縮圖檢視以由右至左、由上到下的方向填入。 </p> <p>設定<span class="codeph">自動</span>時，當地區設定設為<span class="codeph"> ja時，檢視器套用<span class="codeph">右</span>模式；</span>否則，它使用<span class="codeph">左</span>模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-a66ce10d6c0b449883f654e7e0657e2c}

選擇性.

## 預設 {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## 範例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
