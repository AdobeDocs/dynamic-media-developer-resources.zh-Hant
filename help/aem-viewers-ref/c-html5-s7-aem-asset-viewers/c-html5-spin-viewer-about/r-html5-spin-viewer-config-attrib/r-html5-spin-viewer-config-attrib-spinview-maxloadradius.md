---
description: 'null'
seo-description: 'null'
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 表示當回轉視圖空閒時，要在每個方向上預載的幀數上限。 值-1 <span class="codeph"> 預載集中</span> 的所有幀。 預先載入的影格一律以SpinView最初載入的原始解析度顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 控制預先載入影格的品質。 當設為 <span class="codeph"> 1</span> 個畫格時，會以高品質載入，以符合元件的大小。 設為 <span class="codeph"> 0</span> 時，只會載入低解析度預覽圖格。 </p> <p>以高解析度預載可改善使用者體驗，尤其是在啟用自動回轉時。 同時，它會導致啟動時間變慢、網路消耗量增加，因此請謹慎使用。 當使用高解析度預載時，預載的幀始終處於元件最初載入時的原始解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
