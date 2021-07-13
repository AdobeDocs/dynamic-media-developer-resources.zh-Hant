---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 </p> <p> 當設定為<span class="codeph"> up </span>、<span class="codeph"> down </span>、<span class="codeph"> left </span>或<span class="codeph"> right </span>時，面板沿指定方向滾動，無需進行其他界限檢查。 此行為可能導致外部容器剪裁面板。 </p> <p>當設為<span class="codeph"> fit-vertical </span>時，元件會先將基礎面板位置移至SocialShare的底部，並嘗試從底部、右側或左側展開面板。 每次嘗試時，元件都會檢查面板是否被外部容器剪下。 如果所有嘗試均失敗，則元件會嘗試將基板位置移到頂部，然後從上、右和左方向重複展開嘗試。 </p> <p>當設為<span class="codeph"> fit-lateral </span>時，元件使用與fit-vertical類似的邏輯，但是會將底座向右、向下和向上移開，然後將底座向左移開，再向左移開，再向左、向下和向上移開。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8e843b967237426e9a8b3cd0f27b9820}

選填。

## 預設 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 範例 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
