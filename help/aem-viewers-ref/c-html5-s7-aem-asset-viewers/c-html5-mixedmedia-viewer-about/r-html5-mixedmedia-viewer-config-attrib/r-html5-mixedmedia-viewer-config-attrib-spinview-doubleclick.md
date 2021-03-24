---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media經典，檢視器，SDK/API,Mix Media Sets
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置按兩下／點選到回轉操作的映射。 設為<span class="codeph"> none </span>會停用雙鍵／點選回轉。 如果設定為<span class="codeph">縮放</span>，按一下影像會在單一旋轉步驟中旋轉；CTRL+Click可旋轉一個回轉步驟。 設為<span class="codeph"> reset </span>會讓您在影像上按一下滑鼠，將回轉重設為初始回轉層級。 對於<span class="codeph"> zoomReset </span>，如果當前回轉系數達到或超過指定的限制，則會套用重設，否則會套用回轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 在桌上型電腦上； `zoomReset` 觸控式裝置。

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
