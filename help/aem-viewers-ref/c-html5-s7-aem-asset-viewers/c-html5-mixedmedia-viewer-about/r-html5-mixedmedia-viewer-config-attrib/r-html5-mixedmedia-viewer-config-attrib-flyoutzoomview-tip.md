---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic media
uuid: 16a0ca99-1ed5-4f1d-b068-55adc46fde0b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持續時間`*[, *``*][, *`計數`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 指定提示文本在隱藏之前顯示的秒數。 設為-1 <span class="codeph"> 時</span>，即使使用者啟動彈出畫面，訊息仍一律顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定在檢視集合中的新影像時顯示文字的次數。 值-1表 <span class="codeph"> 示</span> ，在檢視集合中的任何影像時，一律會顯示文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 淡化</span></span> </p> </td> 
   <td colname="col2"> 指定當文字出現或消失時發生的淡化動畫持續時間。 值0表示 <span class="codeph"> 沒有淡入</span> (fade)轉變。 </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
