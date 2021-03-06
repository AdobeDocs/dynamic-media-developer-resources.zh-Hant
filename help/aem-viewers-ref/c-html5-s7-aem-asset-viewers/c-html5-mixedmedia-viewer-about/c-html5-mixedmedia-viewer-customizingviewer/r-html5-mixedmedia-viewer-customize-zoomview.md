---
title: 縮放視圖
description: 在連續縮放模式下，當當前資產是單個影像時，主視圖由可縮放影像組成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# 縮放視圖{#zoom-view}

在連續縮放模式下，當當前資產是單個影像時，主視圖由可縮放影像組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

查看區域的外觀由以下CSS類選擇器控制：

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
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 主視圖的十六進位格式背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 游標 </span> </p> </td> 
   <td colname="col2"> <p>顯示在主視圖上的游標。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使縮放視圖透明。

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

在台式機系統上，該元件支援 `cursortype` 屬性選擇器，可應用於 `.s7zoomview` 類。 它根據元件狀態和用戶操作控制游標的類型。 以下 `cursortype` 值受支援：

* `default`

   當由於影像解析度較低或元件設定或兩者都導致無法縮放影像時顯示。

* `zoomin`

   可放大影像時顯示。

* `reset`

   當影像處於最大縮放級別時顯示，並且可以將其重置為初始狀態。

* `drag`

   當用戶平移處於縮放狀態的影像時顯示。

* `slide`

   當用戶通過水準輕掃或輕拂執行影像交換時顯示。
