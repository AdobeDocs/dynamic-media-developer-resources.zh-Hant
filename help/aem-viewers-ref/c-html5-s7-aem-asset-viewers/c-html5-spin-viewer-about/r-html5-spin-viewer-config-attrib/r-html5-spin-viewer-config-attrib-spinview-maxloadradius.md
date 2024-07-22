---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">值</span></span> </p> </td> 
   <td colname="col2"> <p> 表示當「迴轉檢視」閒置時，在每個方向要預先載入的最大影格數。 值為<span class="codeph"> -1</span>會預先載入集中的所有框架。 預先載入影格一律會以「迴轉檢視」最初載入的原始解析度顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">高解析度</span></span> </p> </td> 
   <td colname="col2"> <p> 控制預先載入影格的品質。 設定為<span class="codeph">時，會以高品質載入1</span>個影格，符合元件的大小。 設定為<span class="codeph"> 0</span>時，只會載入低解析度的預覽拼貼。 </p> <p>以高解析度預先載入可改善一般使用者體驗，尤其是在啟用自動迴轉的情況下。 同時，這會使啟動時間變慢，並造成較高的網路耗用量，因此請謹慎使用。 使用高解析度預先載入時，預先載入的影格一律為元件最初載入的原始解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選擇性.

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
