---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media經典，檢視器，SDK/API，回轉集
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置按兩下／點選到回轉操作的映射。 設為<span class="codeph"> none </span>會停用雙鍵／點選回轉。 如果設定為<span class="codeph">縮放</span>，按一下影像會在單一旋轉步驟中旋轉；CTRL+Click可旋轉一個回轉步驟。 設為<span class="codeph"> reset </span>會讓您在影像上按一下滑鼠，將回轉重設為初始回轉層級。 對於<span class="codeph"> zoomReset </span>，如果當前回轉系數達到或超過指定的限制，則會套用重設，否則會套用回轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`reset` 在桌上型電腦上； `zoomReset` 觸控式裝置。

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
