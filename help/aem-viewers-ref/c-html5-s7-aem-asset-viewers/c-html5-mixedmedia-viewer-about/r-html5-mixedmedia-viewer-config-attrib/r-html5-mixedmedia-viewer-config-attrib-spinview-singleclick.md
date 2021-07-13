---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,User
exl-id: 18c5c21d-af31-4b1c-ab8b-c04d08650123
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重設|縮放重設  </span> </p> </td> 
   <td colname="col2"> <p> 設定單按/點選的對應以縮放動作。設為<span class="codeph"> none </span>會停用單按/點選縮放。 如果設為<span class="codeph">縮放</span>按一下影像會縮放一個縮放步驟；按住CTRL鍵並按一下可縮小一個縮放步驟。 將設定為<span class="codeph">重設</span>會使影像上只需按一下，即可將縮放重設為初始自轉層級。 對於<span class="codeph"> zoomReset </span>，如果當前縮放系數達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` 在台式電腦上； `none` 在觸控裝置上。

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
