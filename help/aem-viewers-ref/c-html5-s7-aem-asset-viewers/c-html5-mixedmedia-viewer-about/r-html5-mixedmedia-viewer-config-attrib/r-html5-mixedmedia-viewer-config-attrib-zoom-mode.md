---
description: 設定縮放互動的類型。
solution: Experience Manager
title: zoomMode
feature: Dynamic Media經典，檢視器，SDK/API,Mix Media Sets
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---


# zoomMode{#zoommode}

設定縮放互動的類型。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuous可 </span> 讓您在主檢視中按一下、點選兩下或夾捏影像時，在影像逐漸放大的位置進行傳統縮放。您必須明確縮小或重設縮放狀態，才能返回初始檢視。 </p> <p> <span class="codeph"> 內嵌 </span> 功能可讓您立即縮放，當您將主檢視暫留在桌上型電腦或觸控式裝置上時，縮放的影像會立即出現；當您從檢視中移動滑鼠或鬆開手指時，影像會自動回復為初始狀態。請注意，在<span class="codeph">內嵌</span>模式中，巢狀影像集會平面化並顯示為個別縮圖。 <span class="codeph"> 自動 </span> 在桌上型電腦上啟動內嵌模式，在觸控裝置上啟動連續模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
