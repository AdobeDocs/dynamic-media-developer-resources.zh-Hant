---
description: 方向
solution: Experience Manager
title: 方向
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 3%

---

# 方向{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動|左|右 </span> </p> </td> 
   <td colname="col2"> <p>指定頁面在主視圖和縮略圖中的顯示方式。 它還指定用戶與查看器用戶介面交互的方式，以在目錄幀之間進行更改。 </p> <p>當 <span class="codeph"> 左 </span> 用於為初始頁設定右對齊，為最後一頁設定左對齊。 它為從左到右的渲染順序縫製各個頁面子影像。 它還設定主視圖以使用從右到左的幻燈片動畫來推進目錄（在情況下） <span class="codeph"> PageView.frametransition </span> )。 最後，為從左到右填充順序設定縮略圖。 </p> <p>同樣，當 <span class="codeph"> 右 </span> 用於為初始頁設定左對齊，為最後一頁設定右對齊。 它針對從右到左的渲染順序對各個頁面子影像進行縫合。 它還設定主視圖以使用從左到右的幻燈片動畫來推進目錄（在情況下） <span class="codeph"> PageView.frametransition </span> )。 最後，它反轉縮略圖順序，以便縮略圖視圖以從右到左、從上到下的方向填充。 </p> <p>當 <span class="codeph"> 自動 </span> 設定，查看器應用 <span class="codeph"> 右 </span> 模式區域設定為 <span class="codeph"> ja; </span>否則，它使用 <span class="codeph"> 左 </span> 的子菜單。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-a66ce10d6c0b449883f654e7e0657e2c}

選擇性.

## 預設 {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## 範例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
