---
description: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 突出顯示|游標  </span> </p> </td> 
   <td colname="col2"> <p> 指定要使用的導航框架的類型。 當設定為<span class="codeph">游標</span>時，元件使用固定大小的參考游標。 案頭系統和觸摸設備可以有不同的游標圖，這可以使用<span class="codeph"> .s7cursor </span> CSS類和<span class="codeph"> input=mouse|touch </span>屬性選擇器進行控制。 在案頭系統上，錨點設定在游標區域的中間，而在觸摸設備上，錨點位於游標的底部中心。 設為<span class="codeph">反白顯示</span>時，元件使用可變大小的導航框架；框架的大小和形狀取決於縮放因子和彈出視圖的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> 設定用戶激活突出顯示或游標後淡入所花的時間（以秒為單位）。 淡入僅適用於觸控裝置；在案頭系統上，元件會忽略它。 </p> <p>淡入會套用至下列UI元素：突出顯示幀，固定游標，覆蓋（在<span class="codeph">覆蓋</span>參數設定為<span class="codeph"> 1 </span>時）。 彈出視圖動畫僅在動畫完成時才開始，突出顯示/游標淡出。 沒有淡出動畫。 當使用者停用彈出視窗時，對應的UI元素（游標、反白顯示和覆蓋）會立即隱藏。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> 控制導航幀定位。 </p> <p>如果在影像</span>上設定為<span class="codeph">，則導航框架只能位於主視圖中的實際影像區域內。 </span></p> <p>如果設定為<span class="codeph">自由</span> ，則用戶可以將導航幀移動到邏輯主視圖區域中的任意位置，甚至在影像內容之外。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
