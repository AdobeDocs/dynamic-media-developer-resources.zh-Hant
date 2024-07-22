---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 2%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 當彈出式視窗為作用中時，控制主檢視反白顯示外觀。 設定為<span class="codeph"> 0</span>時，目前顯示在彈出式視窗中的區域會使用<span class="codeph"> .s7highlight</span>或<span class="codeph"> .s7cursor</span> CSS類別名稱所提供的樣式來反白顯示（取決於<span class="codeph"> highlightmode</span>修飾元的值）。 設定為<span class="codeph">時，1</span>元件進入「反向」模式，目前檢視的區域為完全透明（若<span class="codeph"> highlightmode</span>設定為<span class="codeph"> highlightmode</span>）或使用<span class="codeph"> .s7cursor</span> CSS類別名稱的樣式（若<span class="codeph"> highlightmode</span>設定為<span class="codeph"> cursor</span>），但周圍的區域已使用<span class="codeph"> .s7overlay</span> CSS類別名稱提供的樣式填滿。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選擇性.

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
