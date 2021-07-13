---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic，檢視器，SDK/API，回轉集
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> 表示當SpinView空閒時要在每個方向上預載入的幀數上限。 值<span class="codeph"> -1</span>預載入集中的所有幀。 預載入的幀始終以SpinView最初載入的原始解析度顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 控制預載入幀的質量。 當設定為<span class="codeph"> 1</span>幀以高質量載入時，匹配元件的大小。 當設為<span class="codeph"> 0</span>時，只會載入低解析度預覽圖磚。 </p> <p>以高解析度預先載入可改善一般使用者體驗，尤其是啟用自動回轉時。 同時，它會導致啟動時間變慢和網路消耗增加，因此請謹慎使用。 當使用高解析度預載入時，預載入的幀始終處於元件最初載入時的原始解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
