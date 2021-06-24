---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic，檢視器，SDK/API，回轉集
role: Developer,Business Practitioner
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重設|縮放重設  </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選至回轉動作的對應。 設為<span class="codeph"> none </span>會停用雙按/點選回轉。 如果設為<span class="codeph">縮放</span> ，按一下影像在一個回轉步驟中旋轉；按住CTRL鍵並按一下可旋轉一個回轉步驟。 將設定為<span class="codeph">重設</span>會導致在影像上按一下，將回轉重設為初始回轉層級。 對於<span class="codeph"> zoomReset </span>，如果當前自旋系數達到或超過指定限制，則應用重置，否則應用自旋。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`reset` 在台式電腦上； `zoomReset` 在觸控裝置上。

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
