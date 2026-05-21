---
title: 次要控制列
description: 次要控制列是包含「第一頁」和「最後一頁」按鈕的矩形區域，當在CSS中提供時，還會有「頁面指示器」。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
TQID: 'https://experienceleague.adobe.com/NMaW0QPU2A3pUzpvMg3kbW8MmeLbJ1hZlCSGTEcG6Ko'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 0%

---

# 次要控制列{#secondary-control-bar}

次要控制列是包含「第一頁」和「最後一頁」按鈕的矩形區域，當在CSS中提供時，還會有「頁面指示器」。

依預設，它只會顯示在行動電話的檢視器底部。 它一律會採用整個可用檢視器寬度。 您可以透過CSS變更其相對於檢視器容器的顏色、高度和垂直位置。

次要控制項列的外觀是由下列CSS類別選取器所控制：

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
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
