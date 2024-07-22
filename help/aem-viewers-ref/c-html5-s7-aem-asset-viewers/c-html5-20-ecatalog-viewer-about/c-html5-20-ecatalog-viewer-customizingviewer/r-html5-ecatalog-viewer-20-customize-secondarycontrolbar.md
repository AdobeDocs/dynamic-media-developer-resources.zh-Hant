---
title: 次要控制列
description: 次要控制列是包含「第一頁」和「最後一頁」按鈕的矩形區域，當在CSS中提供時，還會有「頁面指示器」。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 2354c3a0-2df7-4a18-aac1-fac158a9b659
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# 次要控制列{#secondary-control-bar}

次要控制列是包含「第一頁」和「最後一頁」按鈕的矩形區域，當在CSS中提供時，還會有「頁面指示器」。

依預設，其僅會顯示在行動電話上，並位於檢視器的底部。 它一律會採用整個可用檢視器寬度。 您可以透過CSS變更其相對於檢視器容器的顏色、高度和垂直位置。

次要控制項列的外觀是由下列CSS類別選取器所控制：

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>從檢視器頂端的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">後</span> </p> </td> 
   <td colname="col2"> <p>從檢視器底部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>主要控制列的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>次要控制列的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定高為72畫素且位於檢視器容器底部的灰色次要控制列。

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
