---
description: 次要控制列是矩形區域，當在CSS中提供使用時，其中包含「第一頁」和「最後一頁」按鈕以及「頁面指示器」。
solution: Experience Manager
title: 輔助控制條
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 2%

---

# 輔助控制條{#secondary-control-bar}

次要控制列是矩形區域，當在CSS中提供使用時，其中包含「第一頁」和「最後一頁」按鈕以及「頁面指示器」。

依預設，它只會顯示在行動電話上，且位於檢視器底部。 它一律會佔用整個可用的檢視器寬度。 您可以透過CSS相對於檢視器容器來變更其顏色、高度和垂直位置。

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
   <td colname="col2"> <p>從檢視器頂端的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從檢視器底部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主控制欄的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>輔助控制條的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：設定高度為72像素且位於檢視器容器底部的灰色次要控制列。

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
