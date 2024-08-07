---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上|下|左|右|適合 — 垂直|適合 — 橫向</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 </p> <p> 當設定為<span class="codeph"> up </span>，<span class="codeph"> down </span>，<span class="codeph"> left </span>或<span class="codeph"> right </span>時，面板會以指定方向轉出，而不需要額外的界限檢查。 此行為可能會導致面板被外部容器剪裁。 </p> <p>設定為<span class="codeph"> fit-vertical </span>時，元件會先將基礎面板位置移至SocialShare的底部，然後嘗試從此類基礎位置從底部、右側或左側轉出面板。 在每次嘗試時，元件都會檢查面板是否已由外部容器裁剪。 如果所有嘗試都失敗，元件會嘗試將基礎面板位置移至頂端，並從上、右和左方向重複轉出嘗試。 </p> <p>當設定為<span class="codeph">符合橫向</span>時，元件會使用與「符合垂直」類似的邏輯，但會將基底移至右側，先嘗試右、下、上轉出方向，然後將基底移至左側，嘗試左、下、上轉出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8e843b967237426e9a8b3cd0f27b9820}

選擇性.

## 預設 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 範例 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
