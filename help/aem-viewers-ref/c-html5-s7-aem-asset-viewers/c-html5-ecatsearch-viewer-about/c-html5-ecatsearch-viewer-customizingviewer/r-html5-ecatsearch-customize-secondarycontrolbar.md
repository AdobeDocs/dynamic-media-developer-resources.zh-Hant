---
title: 輔助控制欄
description: 輔助控制欄是矩形區域，當在CSS中提供時，該區域包含「第一頁」和「最後一頁」按鈕以及「頁面指示器」。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# 輔助控制欄{#secondary-control-bar}

輔助控制欄是矩形區域，當在CSS中提供時，該區域包含「第一頁」和「最後一頁」按鈕以及「頁面指示器」。

預設情況下，它僅顯示在查看器底部的行動電話上。 它始終佔用整個可用查看器寬度。 可以通過CSS相對於查看器容器更改其顏色、高度和垂直位置。

輔助控制欄的外觀由以下CSS類選擇器控制：

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從查看器頂部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從查看器底部定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主控制欄的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>輔助控制欄的背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定一個灰色輔助控制欄，該欄高72像素，位於查看器容器的底部。

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
