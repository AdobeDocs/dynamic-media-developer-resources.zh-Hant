---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e87981f8-8174-432a-89ea-fae74d0584ad
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|縮放|重置|縮放重置 </span> </p> </td> 
   <td colname="col2"> <p> 配置按兩下/點擊以縮放操作的映射。 設定為 <span class="codeph"> 無 </span> 禁用按兩下/點擊縮放。 如果設定為 <span class="codeph"> 縮放 </span> 按一下影像可縮放一個縮放步驟；CTRL+按一下可縮小一個縮放步驟。 設定為 <span class="codeph"> 重置 </span> 使按一下影像將縮放重置為初始縮放級別。 對於 <span class="codeph"> 縮放重置 </span>，如果當前縮放因子達到或超過指定限制，則應用重置，否則應用縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 在台式電腦上； `zoomReset` 觸摸設備。

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
