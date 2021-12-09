---
title: 方向
description: 指定主視圖和縮圖中頁面的顯示方式。 它也會指定使用者與檢視器使用者介面互動的方式，以便在目錄框架之間變更。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 方向{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>指定主視圖和縮圖中頁面的顯示方式。 它也會指定使用者與檢視器使用者介面互動的方式，以便在目錄框架之間變更。 </p> <p>當 <span class="codeph"> lef </span> 使用時，會為初始頁面設定右對齊方式，並為最後一頁設定左對齊方式。 它可拼接個別頁面子影像，以依照從左到右的轉譯順序。 它還設定主視圖以使用從右到左的幻燈片動畫來推進目錄（在情況下） <span class="codeph"> PageView.frametransition </span> 設為滑動)。 最後，設定左至右填充順序的縮圖。 </p> <p>同樣地，當 <span class="codeph"> 右 </span> 使用時，會為初始頁面設定左對齊方式，並為最後一頁設定右對齊方式。 它會拼接個別頁面子影像，以依從右到左轉譯順序。 它還設定主視圖以使用左到右幻燈片動畫來推進目錄（在情況下） <span class="codeph"> PageView.frametransition </span> 設為滑動)。 最後，它會反轉縮圖順序，使縮圖檢視以由右至左、由上至下的方向填入。 </p> <p>當 <span class="codeph"> 自動 </span> 已設定，則檢視器會套用 <span class="codeph"> 右 </span> 模式 <span class="codeph"> ja; </span>否則，會使用 <span class="codeph"> lef </span> 模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-a66ce10d6c0b449883f654e7e0657e2c}

選填。

## 預設 {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## 範例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
