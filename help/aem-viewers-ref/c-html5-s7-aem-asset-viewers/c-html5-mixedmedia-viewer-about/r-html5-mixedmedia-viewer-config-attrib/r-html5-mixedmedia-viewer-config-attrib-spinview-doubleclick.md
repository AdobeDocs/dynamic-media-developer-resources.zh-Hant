---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重置|縮放重置 </span> </p> </td> 
   <td colname="col2"> <p> 配置按兩下/點擊到旋轉操作的映射。 設定為 <span class="codeph"> 無 </span> 禁用按兩下/點擊旋轉。 如果設定為 <span class="codeph"> 縮放 </span>，按一下影像旋轉一步；CTRL+按一下可旋轉一個旋轉步驟。 設定為 <span class="codeph"> 重置 </span> 使按一下影像將旋轉重置為初始旋轉級別。 對於 <span class="codeph"> 縮放重置 </span>，如果當前自旋因子處於或超過指定限制，則應用reset，否則應用自旋。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 在台式電腦上； `zoomReset` 觸摸設備。

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
