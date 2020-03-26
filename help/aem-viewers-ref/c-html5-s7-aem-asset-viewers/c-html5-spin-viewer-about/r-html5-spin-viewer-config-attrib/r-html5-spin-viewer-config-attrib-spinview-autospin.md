---
description: 'null'
seo-description: 'null'
seo-title: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
topic: Dynamic media
uuid: 9d24ed39-e4b9-442b-bc64-c77707ff69d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`期間directionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 啟用或停用自動回轉動畫。 為獲得最佳的自動回轉體驗，建議您將maxloadradius設定為 <span class="codeph"> -</span> 1以預先載入所有影格 <span class="codeph"></span>。 但請注意，這會增加負載時間並提高頻寬使用率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 每個完整回轉的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 方向</span></span> </p> </td> 
   <td colname="col2"> <p> 旋轉方向為 <span class="codeph"> 0</span> ，旋轉方向 <span class="codeph"> 為1</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 回轉數</span></span> </p> </td> 
   <td colname="col2"> <p> 自動回轉停止前完成的完全旋轉次數。 該數字是浮點數。 若為無 <span class="codeph"> 限自動回轉</span> ，請設定為-1。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
