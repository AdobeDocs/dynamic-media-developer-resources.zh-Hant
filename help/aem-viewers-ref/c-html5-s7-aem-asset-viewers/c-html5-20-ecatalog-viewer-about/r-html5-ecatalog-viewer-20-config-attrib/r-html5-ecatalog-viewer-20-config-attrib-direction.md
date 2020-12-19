---
description: 'null'
seo-description: 'null'
seo-title: 方向
solution: Experience Manager
title: 方向
topic: Dynamic media
uuid: 185824c5-d6f2-4e1b-99ac-726a295ec5f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---


# 方向{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>指定頁面在主檢視和縮圖中的顯示方式。 它還指定用戶與查看器用戶介面交互的方式，以便在目錄框架之間進行更改。 </p> <p>當使用<span class="codeph"> left </span>時，它會為初始頁面設定右對齊，並為最後一頁設定左對齊。 它可針對個別頁面子影像，依從左至右的轉譯順序進行接合。 它還將主視圖設定為使用由右到左幻燈片動畫來推進目錄（在<span class="codeph"> PageView.frametransition </span>設定為slide的情況下）。 最後，縮圖會依從左至右的填色順序設定。 </p> <p>同樣地，當使用<span class="codeph"> right </span>時，它會為初始頁面設定左對齊，並為最後一頁設定右對齊。 它可針對個別頁面子影像，依從右至左的轉譯順序進行接合。 它還將主視圖設定為使用從左到右幻燈片動畫來推進目錄（在<span class="codeph"> PageView.frametransition </span>設定為slide的情況下）。 最後，它會反轉縮圖順序，讓縮圖檢視以從右到左、從上到下的方向填入。 </p> <p>設定<span class="codeph"> auto </span>時，當地區設定設為<span class="codeph"> ja；時，檢視器會套用<span class="codeph"> right </span>模式；</span>否則，它使用<span class="codeph">左</span>模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-a66ce10d6c0b449883f654e7e0657e2c}

選填。

## 預設 {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## 範例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
