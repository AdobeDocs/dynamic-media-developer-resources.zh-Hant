---
description: 指定按鈕容器的幻燈片動畫方向。
solution: Experience Manager
title: Favoritemenu.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
TQID: 'https://experienceleague.adobe.com/Pe9frhI8cmIorx5zE-cdC-frEP77UOksMwyM9PvUCdo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# Favoritemenu.bearing{#favoritesmenu-bearing}

指定按鈕容器的幻燈片動畫方向。

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">上|下|左|右|fit — 垂直|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 當設定為<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>時，面板會以指定方向轉出，而不需要額外的界限檢查，導致面板被外部容器剪裁。 </p> <p>設定為<span class="codeph"> fit-vertical</span>時，元件會先將基礎面板位置移至「我的最愛」功能表的底部，並嘗試從此類基礎位置以下列方向之一轉出面板：底部、右側、左側。 在每次嘗試時，元件都會檢查面板是否被外部容器裁剪。 如果所有嘗試都失敗，元件會嘗試將基礎面板位置移至頂端，並從上、右和左方向重複轉出嘗試。 </p> <p>當設定為<span class="codeph"> fit-lateral</span>時，元件會使用類似的邏輯。 基底會先向右移動，嘗試向右、向下和向上轉出方向。 然後，它會將基底向左移動，嘗試向左、向下和向上轉出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]

