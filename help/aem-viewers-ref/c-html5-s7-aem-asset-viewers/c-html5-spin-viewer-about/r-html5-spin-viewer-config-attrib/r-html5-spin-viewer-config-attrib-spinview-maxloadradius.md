---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`值`*[, *`高Res`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 表示SpinView空閒時在每個方向上要預載入的最大幀數。 值 <span class="codeph"> -1</span> 預載集中的所有幀。 預載幀始終以SpinView最初載入的原始解析度顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高Res</span></span> </p> </td> 
   <td colname="col2"> <p> 控制預載幀的質量。 設定為時 <span class="codeph"> 1</span> 幀以高質量載入，與元件大小匹配。 設定為時 <span class="codeph"> 0</span> 只載入低解析度預覽平鋪。 </p> <p>以高解析度預載入可改善最終用戶體驗，特別是當啟用自動旋轉時。 同時，它會導致啟動時間較慢，網路消耗也較高，因此應謹慎使用。 當使用高解析度預載時，預載幀始終處於元件初始載入時的原始解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
