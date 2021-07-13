---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 當彈出活動時，控制主視圖突出顯示外觀。 設為<span class="codeph"> 0</span>時，使用<span class="codeph"> .s7highlight</span>或<span class="codeph"> .s7cursor</span> CSS類名稱提供的樣式（取決於<span class="codeph"> highlightmode</span>修飾符的值）來突出顯示彈出窗口中當前可見的區域。 當設定為<span class="codeph"> 1</span>元件進入「反向」模式時，當前查看區域為完全透明（在<span class="codeph">高亮模式</span>設定為<span class="codeph">高亮模式</span>時）或設定為<span class="codeph"> .s7cursor</span> CSS類名（在<span class="codeph">高亮模式</span>設定為<span class="codeph"></span>時），但周圍區域使用<span class="codeph"></span>提供的樣式填充CSS類名。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
