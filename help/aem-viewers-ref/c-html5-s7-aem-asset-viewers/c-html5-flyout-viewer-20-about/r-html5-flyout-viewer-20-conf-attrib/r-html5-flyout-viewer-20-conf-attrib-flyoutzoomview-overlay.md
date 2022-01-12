---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 當彈出活動時，控制主視圖突出顯示外觀。 設為時 <span class="codeph"> 0</span>，則會使用提供的樣式來反白顯示彈出視窗中目前可見的區域 <span class="codeph"> .s7highlight</span> 或 <span class="codeph"> .s7cursor</span> CSS類名(取決於 <span class="codeph"> 高光模式</span> 修飾詞)。 設為時 <span class="codeph"> 1</span> 元件進入「反向」模式，其中目前檢視的區域為完全透明（在情況下） <span class="codeph"> 高光模式</span> 設為 <span class="codeph"> 醒目提示</span>)或 <span class="codeph"> .s7cursor</span> CSS類名(大小寫 <span class="codeph"> 高光模式</span> 設為 <span class="codeph"> 游標</span>)，但周圍區域會使用 <span class="codeph"> .s7覆蓋</span> CSS類名。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
