---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重置|縮放重置 </span> </p> </td> 
   <td colname="col2"> <p> 配置按一下/點擊的映射以縮放操作。設定為 <span class="codeph"> 無 </span> 禁用按一下/點擊縮放。 如果設定為 <span class="codeph"> 自旋 </span> 按一下影像可縮放一個縮放步驟；CTRL+按一下可縮小一個縮放步驟。 設定為 <span class="codeph"> 重置 </span> 使按一下影像將縮放重置為初始旋轉級別。 對於 <span class="codeph"> 縮放重置 </span>，如果當前縮放因子達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` 在台式電腦上； `none` 觸摸設備。

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
