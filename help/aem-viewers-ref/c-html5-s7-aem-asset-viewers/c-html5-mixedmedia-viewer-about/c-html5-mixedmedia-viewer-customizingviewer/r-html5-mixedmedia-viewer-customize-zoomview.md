---
description: 在連續縮放模式中，當目前資產是單一影像時，主檢視會由可縮放的影像組成。
solution: Experience Manager
title: 縮放檢視
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---


# 縮放視圖{#zoom-view}

在連續縮放模式中，當目前資產是單一影像時，主檢視會由可縮放的影像組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

檢視區域的外觀會使用下列CSS類別選擇器加以控制：

```
.s7mixedmediaviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p> 主視圖的十六進位格式背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 游標  </span> </p> </td> 
   <td colname="col2"> <p>顯示在主視圖上的游標。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——使縮放視圖透明。

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

在案頭系統上，元件支援`cursortype`屬性選擇器，該選擇器可應用於`.s7zoomview`類。 它根據元件狀態和用戶操作控制游標的類型。 支援下列`cursortype`值：

* `default`

   當影像因影像解析度小或元件設定或兩者皆無法縮放時顯示。

* `zoomin`

   可放大影像時顯示。

* `reset`

   當影像處於最大縮放層級，且可重設為初始狀態時顯示。

* `drag`

   當使用者平移處於縮放狀態的影像時顯示。

* `slide`

   當使用者透過水準滑動或輕拂來執行影像切換時顯示。

