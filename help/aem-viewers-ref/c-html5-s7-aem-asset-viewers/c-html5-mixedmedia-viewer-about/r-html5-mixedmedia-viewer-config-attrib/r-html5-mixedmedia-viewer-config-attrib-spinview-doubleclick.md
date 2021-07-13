---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重設|縮放重設  </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選至回轉動作的對應。 設為<span class="codeph"> none </span>會停用雙按/點選回轉。 如果設為<span class="codeph">縮放</span> ，按一下影像在一個回轉步驟中旋轉；按住CTRL鍵並按一下可旋轉一個回轉步驟。 將設定為<span class="codeph">重設</span>會導致在影像上按一下，將回轉重設為初始回轉層級。 對於<span class="codeph"> zoomReset </span>，如果當前自旋系數達到或超過指定限制，則應用重置，否則應用自旋。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 在台式電腦上； `zoomReset` 在觸控裝置上。

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
