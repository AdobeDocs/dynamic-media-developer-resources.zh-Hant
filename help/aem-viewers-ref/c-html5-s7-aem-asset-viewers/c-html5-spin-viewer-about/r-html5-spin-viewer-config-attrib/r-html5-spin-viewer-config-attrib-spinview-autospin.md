---
description: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
uuid: 9d24ed39-e4b9-442b-bc64-c77707ff69d8
feature: Dynamic Media經典，檢視器，SDK/API，回轉集
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 6%

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`期間directionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 啟用或停用自動回轉動畫。 為獲得最佳的自動回轉體驗，建議您將<span class="codeph"> maxloadradius</span>設為<span class="codeph"> -1</span>，以預先載入所有影格。 但請注意，這會增加負載時間並提高頻寬使用率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 每個完整回轉的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 方向</span></span> </p> </td> 
   <td colname="col2"> <p> 旋轉向東方向為<span class="codeph">0</span>，旋轉向西方向為<span class="codeph">1</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 回轉數</span></span> </p> </td> 
   <td colname="col2"> <p> 自動回轉停止前完成的完全旋轉次數。 該數字是浮點數。 對於無限自動旋轉，設定為<span class="codeph"> -1</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
