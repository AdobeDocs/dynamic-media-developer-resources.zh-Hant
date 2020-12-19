---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 當彈出活動時，控制主視圖反白顯示外觀。 當設為<span class="codeph"> 0</span>時，會使用<span class="codeph"> .s7highlight</span>或<span class="codeph"> .s7cursor</span> CSS類別名稱（視<span class="codeph"> highlightmode</span>修飾詞的值而定）提供的樣式，反白標示目前在彈出視窗中可見的區域。 當設為<span class="codeph"> 1</span>元件時，進入「反向」模式，其中目前檢視的區域為完全透明（在<span class="codeph"> highlightmode</span>設為<span class="codeph"> highlight</span>時）或以<span class="codeph"> .s7cursor</span> CSS類別名稱（在<span class="codeph"> highlightmode</span>中）設為<span class="codeph"> cursor</span>)，但使用<span class="codeph"> .s7overlay</span> CSS類別名稱提供的樣式填入周圍區域。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
