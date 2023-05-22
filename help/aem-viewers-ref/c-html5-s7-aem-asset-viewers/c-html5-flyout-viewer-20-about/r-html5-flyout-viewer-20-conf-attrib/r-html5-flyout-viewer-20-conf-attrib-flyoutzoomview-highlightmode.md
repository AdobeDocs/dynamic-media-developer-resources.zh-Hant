---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`顯示時間`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 突出顯示|游標 </span> </p> </td> 
   <td colname="col2"> <p> 指定要使用的導航框架的類型。 設定為時 <span class="codeph"> 游標 </span>，該元件使用固定大小的引用游標。 對於台式機系統和觸摸設備，可以使用不同的游標藝術。 此能力由 <span class="codeph"> .s7游標 </span> CSS類和 <span class="codeph"> 輸入=滑鼠|觸摸 </span> 屬性選擇器。 在台式機系統上，在游標區域的中間設定一個錨點，而在觸摸設備上，錨點位於游標的下中心。 設定為時 <span class="codeph"> 突出顯示 </span>，元件使用可變大小的導航框架；框架的大小和形狀取決於縮放因子和彈出視圖的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 顯示時間 </span> </span> </p> </td> 
   <td colname="col2"> <p> 設定用戶激活高光或游標後淡入所需的時間（秒）。 淡入僅應用於觸摸設備；在案頭系統上，該元件將忽略它。 </p> <p>淡入適用於以下UI元素：高亮幀，固定游標，覆蓋（在情況下） <span class="codeph"> 覆蓋 </span> 參數設定為 <span class="codeph"> 1 </span>)。 浮動視圖動畫僅在動畫完成高亮/游標淡出後開始。 沒有淡出動畫。 當用戶停用彈出功能時，相應的UI元素（游標、高亮和覆蓋）會立即隱藏。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> 控制導航框架定位。 </p> <p>如果設定為 <span class="codeph"> 影像 </span>，導航框架只能位於主視圖內實際影像區域內。 </p> <p>如果設定為 <span class="codeph"> 免費 </span> 用戶可以將導航框架移動到邏輯主視圖區域中的任意位置，即使是外部影像內容。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選擇性.

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
