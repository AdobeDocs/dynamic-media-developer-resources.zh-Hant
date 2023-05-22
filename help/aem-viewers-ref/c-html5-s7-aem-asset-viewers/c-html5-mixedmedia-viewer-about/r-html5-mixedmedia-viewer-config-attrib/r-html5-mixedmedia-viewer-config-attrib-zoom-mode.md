---
title: 縮放模式
description: 設定縮放交互的類型。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# 縮放模式{#zoommode}

設定縮放交互的類型。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 連續|內聯|自動 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 連續 </span> 在主視圖中按一下、按兩下或收縮時，啟用影像逐漸放大的經典縮放。 要返回到初始視圖，請縮小或重置縮放狀態。 類 </p> <p> <span class="codeph"> 內 </span> 啟用即時縮放，在案頭上懸停主視圖或觸摸和握持觸摸設備時，縮放影像會立即出現。 當您將滑鼠從視圖中移動或鬆開手指後，影像將自動恢復為初始狀態。 在 <span class="codeph"> 內 </span> 模式下，嵌套影像集被平展並顯示為單個縮略圖。 類 <span class="codeph"> 自動 </span> 在案頭上激活串聯模式，在觸摸設備上激活連續模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
