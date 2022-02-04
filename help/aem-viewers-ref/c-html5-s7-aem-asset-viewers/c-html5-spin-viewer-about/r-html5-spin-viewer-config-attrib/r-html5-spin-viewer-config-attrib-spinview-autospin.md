---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`持續時間`*][, *`方向`*][, *`旋轉數`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 啟用或禁用自動旋轉動畫。 為獲得最佳的自動旋轉體驗，建議通過設定 <span class="codeph"> 最大載荷半徑</span> 至 <span class="codeph"> -1</span>。 但是，請注意，此設定會增加負載時間並提高頻寬利用率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 每次完整旋轉的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 方向</span></span> </p> </td> 
   <td colname="col2"> <p> 旋轉方向 <span class="codeph"> 0</span> 轉向東方 <span class="codeph"> 1</span> 向西旋轉。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 旋轉數</span></span> </p> </td> 
   <td colname="col2"> <p> 自動旋轉停止前完成的完全旋轉數。 該數字是浮點數。 設定為 <span class="codeph"> -1</span> 無限自轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
