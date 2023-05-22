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
ht-degree: 3%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 當浮出激活時，控制主視圖的加亮外觀。 設定為時 <span class="codeph"> 0</span>，使用由提供的樣式加亮顯示彈出窗口中當前可見的區域 <span class="codeph"> .s7突出顯示</span> 或 <span class="codeph"> .s7游標</span> CSS類名(取決於 <span class="codeph"> 高光模式</span> 修改量)。 設定為時 <span class="codeph"> 1</span> 元件進入「逆」模式，此時當前查看的區域要麼完全透明（在情況下） <span class="codeph"> 高光模式</span> 設定為 <span class="codeph"> 突出顯示</span>)或 <span class="codeph"> .s7游標</span> CSS類名(以防 <span class="codeph"> 高光模式</span> 設定為 <span class="codeph"> 游標</span>)，但使用由 <span class="codeph"> .s7覆蓋</span> CSS類名。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選擇性.

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
