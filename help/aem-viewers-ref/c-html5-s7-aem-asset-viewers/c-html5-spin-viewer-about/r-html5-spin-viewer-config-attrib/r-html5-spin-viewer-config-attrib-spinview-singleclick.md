---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 設定單鍵／點選對應至縮放動作。設為<span class="codeph">無</span>會停用單鍵／點選縮放。 如果設定為<span class="codeph">回轉</span>按一下影像，會縮放一個縮放步驟；CTRL+Click可縮小一個縮放步驟。 設定為<span class="codeph"> reset </span>會讓您在影像上按一下滑鼠，將縮放重設為初始回轉層級。 對於<span class="codeph"> zoomReset </span>，如果目前的縮放系數達到或超過指定的限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` 在桌上型電腦上； `none` 觸控式裝置。

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
