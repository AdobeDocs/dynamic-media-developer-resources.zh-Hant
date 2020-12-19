---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor  </span> </p> </td> 
   <td colname="col2"> <p> 指定要使用的導覽影格類型。 當設定為<span class="codeph">游標</span>時，元件使用固定大小的參考游標。 案頭系統和觸控裝置可能有不同的游標圖，此圖可使用<span class="codeph"> .s7cursor </span> CSS類別和<span class="codeph"> input=mouse|touch </span>屬性選擇器加以控制。 在案頭系統上，錨點設定在游標區域的中央，而在觸控裝置上，錨點設定在游標的底部中心。 當設為<span class="codeph">反白顯示</span>時，元件會使用可變大小的導覽畫格；影格的大小和形狀取決於縮放系數和彈出檢視的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> 設定在使用者啟動反白顯示或游標後淡入的時間（以秒為單位）。 淡入僅適用於觸控裝置；在案頭系統上，此元件會忽略。 </p> <p>淡入會套用至下列UI元素：反白顯示影格、固定游標、覆蓋（在<span class="codeph">覆蓋</span>參數設為<span class="codeph"> 1 </span>的情況下）。 彈出檢視動畫只會在動畫完成時反白顯示／游標淡入淡出。 沒有淡出動畫。 當使用者停用彈出功能時，對應的UI元素（游標、反白顯示和覆蓋）會立即隱藏。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> 控制導覽影格的位置。 </p> <p>如果設為<span class="codeph"> onimage </span>，則導覽影格只能位於主檢視的實際影像區域內。 </p> <p>如果設為<span class="codeph">免費</span>，則用戶可以將導航框架移動到邏輯主視圖區域中的任意位置，甚至是外部影像內容。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
