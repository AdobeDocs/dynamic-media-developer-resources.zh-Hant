---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選以迴轉動作的對應。 設定為 <span class="codeph"> 無 </span> 停用按兩下/點選迴轉。 若設為 <span class="codeph"> 縮放 </span>，按一下影像會旋轉一個旋轉步驟；按住Ctrl鍵並按一下滑鼠可旋轉一個旋轉步驟。 設定為 <span class="codeph"> 重設 </span> 使得按一下影像即可將迴轉重設為初始迴轉等級。 對象 <span class="codeph"> zoomReset </span>，若目前迴轉因數達到或超過指定限制，則會套用重設，否則會套用迴轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選擇性.

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`reset` 在桌上型電腦上； `zoomReset` 在觸控裝置上。

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
