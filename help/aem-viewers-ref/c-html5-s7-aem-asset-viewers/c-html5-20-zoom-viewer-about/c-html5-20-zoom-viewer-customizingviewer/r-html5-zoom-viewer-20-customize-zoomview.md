---
title: 縮放檢視
description: 主檢視包含可縮放的影像。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
TQID: 'https://experienceleague.adobe.com/i1B2r5g74xmk6H3DLD12gyRI9uJo32p3SmgS-OFnLf8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 0%

---

# 縮放檢視{#zoom-view}

主檢視包含可縮放的影像。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主要檢視器區域的&#x200B;**CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7zoomviewer .s7zoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p> 主檢視的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">游標</span> </p> </td> 
   <td colname="col2"> <p>游標顯示在主檢視上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 讓主檢視透明。

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

在桌上型電腦系統上，元件支援`cursortype`屬性選取器，可套用至`.s7zoomview`類別。 它根據元件狀態和使用者動作來控制游標型別。 支援下列`cursortype`個值：

* `default`

  當影像因為影像解析度較小或元件設定（或兩者）而無法縮放時顯示。

* `zoomin`

  當影像可以放大時顯示。

* `reset`

  當影像處於最大縮放等級時顯示，並可重設為初始狀態。

* `drag`

  當使用者平移處於放大狀態的影像時顯示。

* `slide`

  當使用者透過進行水準撥動或輕觸來執行影像交換時顯示。
