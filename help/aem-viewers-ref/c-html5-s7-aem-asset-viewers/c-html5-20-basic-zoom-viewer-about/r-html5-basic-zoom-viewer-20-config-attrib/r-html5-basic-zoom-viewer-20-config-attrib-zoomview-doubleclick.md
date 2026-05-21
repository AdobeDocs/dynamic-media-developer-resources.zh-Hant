---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 38c90d7f-ddbc-4123-b90d-02f9cabd785c
TQID: 'https://experienceleague.adobe.com/Q68UDbUhC3glR3w6nlXxHFCUlKNbLaNooxP4lcSCBCw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選以縮放動作的對應。 設定為<span class="codeph">無</span>會停用按兩下/點選縮放。 若設為<span class="codeph">縮放</span>，按一下影像可放大一個步階單位；按住Ctrl鍵並按一下滑鼠可縮小一個步階單位。 設定為<span class="codeph">重設</span>會導致按一下影像即可將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果目前縮放因數達到或超過指定限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選擇性.

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`reset`在桌上型電腦上；`zoomReset`在觸控裝置上。

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
