---
description: 次要控制列是矩形區域，當CSS中提供時，該區域會包含「第一頁」和「最後一頁」按鈕，以及「頁面指示器」。
solution: Experience Manager
title: 次控制列
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# 輔助控制條{#secondary-control-bar}

次要控制列是矩形區域，當CSS中提供時，該區域會包含「第一頁」和「最後一頁」按鈕，以及「頁面指示器」。

依預設，它只會顯示在行動電話上，並位於檢視器底部。 它一律會佔用整個可用檢視器寬度。 您可以透過CSS相對於檢視器容器來變更其顏色、高度和垂直位置。

次要控制列的外觀是使用下列CSS類別選擇器來控制：

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
   <td colname="col2"> <p>主控制條的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>次控制欄的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——設定高度為72像素且位於檢視器容器底部的灰色次要控制列。

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

