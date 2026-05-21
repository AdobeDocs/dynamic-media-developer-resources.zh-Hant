---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
TQID: 'https://experienceleague.adobe.com/MvEoXp0DRokxvbSt00t8XdgD3dAxEqylyJ2AD6GvJ5g'
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

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按一下/點選以縮放動作的對應。 設定為<span class="codeph">無</span>會停用按一下/點選縮放。 若設為<span class="codeph">縮放</span>，按一下影像可放大一個步階單位；按住Ctrl鍵並按一下滑鼠可縮小一個步階單位。 設定為<span class="codeph">重設</span>會導致按一下影像即可將縮放重設為初始縮放等級。 對於<span class="codeph"> zoomReset </span>，如果目前縮放因數達到或超過指定限制，則會套用重設，否則會套用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`zoomReset` — 在桌上型電腦上； `none`在觸控裝置上。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
