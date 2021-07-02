---
description: 設定縮放交互的類型。
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# zoomMode{#zoommode}

設定縮放交互的類型。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuous可 </span> 啟用傳統縮放，在您按一下、點選兩下或在主檢視中縮小影像時，影像會逐漸放大。您需要明確縮小或重設縮放狀態，才能返回初始檢視。 </p> <p> <span class="codeph"> 內嵌 </span> 可讓您立即縮放，當您將滑鼠游標暫留在桌上型電腦的主檢視畫面上，或在觸控裝置上觸控並按住時，縮放的影像會立即顯示；當您將滑鼠從視圖中移動或鬆開手指時，影像會自動回復為初始狀態。請注意，在<span class="codeph">內嵌</span>模式中，巢狀影像集會平面化，並顯示為個別縮圖。 <span class="codeph"> 自動 </span> 啟用案頭上的內嵌模式和觸控裝置上的連續模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
