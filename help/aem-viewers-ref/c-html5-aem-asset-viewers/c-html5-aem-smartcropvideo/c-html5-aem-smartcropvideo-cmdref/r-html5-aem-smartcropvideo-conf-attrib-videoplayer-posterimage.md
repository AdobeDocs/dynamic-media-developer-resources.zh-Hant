---
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
title: SmartCropVideoPlayer.posterimage
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

智慧型裁切視訊檢視器的設定屬性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 在視訊開始播放前要在第一個影格上顯示的影像，已針對解析 <span class="codeph"> serverurl</span>. 若在URL中指定，請以HTTP編碼： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>若 <span class="codeph"><span class="varname"> image_id</span></span> 值時，元件會嘗試針對該資產使用預設海報影像。 </p> <p>當視訊指定為路徑時，預設海報影像目錄id會從視訊路徑衍生為 <span class="codeph"> catalog_id/image_id</span> 配對 <span class="codeph"> catalog_id</span> 對應至路徑中的第一個代號，而 <span class="codeph"> image_id</span> 是已移除擴充功能的視訊名稱。 如果具有該ID的影像不存在，則不會顯示海報影像。 </p> <p>若要防止顯示預設海報影像，請指定 <span class="codeph"> 無</span> 作為海報影像值。 如果 <span class="codeph"><span class="varname"> isCommands</span></span> 指定後，在顯示影像之前，命令將應用於預設海報影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

無。

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
