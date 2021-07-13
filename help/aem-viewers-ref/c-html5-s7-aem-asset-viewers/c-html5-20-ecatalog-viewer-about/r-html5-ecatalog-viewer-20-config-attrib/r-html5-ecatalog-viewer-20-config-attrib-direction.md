---
description: 方向
solution: Experience Manager
title: 方向
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---

# 方向{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>指定主視圖和縮圖中頁面的顯示方式。 它也會指定使用者與檢視器使用者介面互動的方式，以便在目錄框架之間變更。 </p> <p>使用<span class="codeph">左</span>時，會為初始頁面設定右對齊方式，為最後一頁設定左對齊方式。 它可拼接個別頁面子影像，以依照從左到右的轉譯順序。 它還設定主視圖以使用從右到左幻燈片動畫來推進目錄（在<span class="codeph"> PageView.frametransition </span>設定為幻燈片時）。 最後，設定左至右填充順序的縮圖。 </p> <p>同樣地，使用<span class="codeph">右</span>時，會為初始頁面設定左對齊方式，為最後一頁設定右對齊方式。 它可拼接個別頁面子影像，以依從右至左轉譯順序。 它還設定主視圖以使用左到右幻燈片動畫來推進目錄（在<span class="codeph"> PageView.frametransition </span>設定為幻燈片時）。 最後，它會反轉縮圖順序，使縮圖檢視以由右至左、由上至下的方向填入。 </p> <p>設定<span class="codeph"> auto </span>時，當區域設定為<span class="codeph"> ja時，查看器將<span class="codeph">向</span>模式應用;</span>否則，會使用左</span>模式的<span class="codeph">。 </span></p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-a66ce10d6c0b449883f654e7e0657e2c}

選填。

## 預設 {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## 範例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
