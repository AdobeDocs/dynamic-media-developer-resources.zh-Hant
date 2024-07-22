---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上|下|左|右|適合 — 垂直|適合 — 橫向</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 </p> <p> 當設定為<span class="codeph"> up </span>，<span class="codeph"> down </span>，<span class="codeph"> left </span>或<span class="codeph"> right </span>時，面板會以指定方向轉出，而不會有額外的界限檢查。 此行為可能會導致面板被外部容器剪裁。 </p> <p>設定為<span class="codeph"> fit-vertical </span>時，元件會先將基礎面板位置移至SocialShare的底部，然後嘗試從此類基礎位置從底部、右側或左側轉出面板。 每次嘗試時，元件都會檢查面板是否被外部容器裁剪。 如果所有嘗試都失敗，元件會嘗試將基礎面板位置移至頂端，並從上、右和左方向重複轉出嘗試。 </p> <p>當設定為<span class="codeph"> fit-lateral </span>時，元件會使用與fit-vertical類似的邏輯。 但是，它會先將基底向右移動，然後向右、向下、向上轉出方向，然後將基底向左移動，再嘗試向左、向下、向上轉出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8e843b967237426e9a8b3cd0f27b9820}

選擇性.

## 預設 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 範例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
