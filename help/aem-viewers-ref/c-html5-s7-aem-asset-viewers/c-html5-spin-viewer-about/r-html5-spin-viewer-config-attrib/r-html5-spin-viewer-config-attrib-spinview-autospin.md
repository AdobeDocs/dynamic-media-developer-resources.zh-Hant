---
description: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
feature: Dynamic Media Classic，檢視器，SDK/API，回轉集
role: Developer,Business Practitioner
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 6%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`durationdirectionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 啟用或禁用自動回轉動畫。 若要獲得最佳的自動回轉體驗，建議您將<span class="codeph"> maxloadradius</span>設定為<span class="codeph"> -1</span>以預先載入所有幀。 但是，請注意，這會增加負載時間並提高頻寬使用量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 每次完全回轉的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 方向</span></span> </p> </td> 
   <td colname="col2"> <p> 旋向為<span class="codeph"> 0</span>，旋向為<span class="codeph"> 1</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 回轉數</span></span> </p> </td> 
   <td colname="col2"> <p> 自動回轉停止前完成的完全旋轉次數。 該數字是浮點數。 設為<span class="codeph"> -1</span>以取得無限自動回轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
