---
title: VideoPlayer.posterimage
description: 視頻查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

視頻查看器的配置屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`影像ID`*][? *`是命令`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|[<span class="varname"> 影像ID</span>][?<span class="varname"> 是命令</span>]</span> </p> </td> 
   <td colname="col2"> <p> 在視頻開始播放之前要在第一幀上顯示的影像，針對 <span class="codeph"> 伺服器url</span>。 如果在URL中指定，則HTTP-encode如下： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 如 <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> 如 <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> 如 <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>如果 <span class="codeph"><span class="varname"> 影像ID</span></span> 值被省略，元件將嘗試使用該資產的預設海報影像。 </p> <p>當視頻被指定為路徑時，預設海報影像目錄ID將從視頻路徑派生為 <span class="codeph"> catalog_id/image_id</span> 配對 <span class="codeph"> 目錄ID</span> 與路徑中的第一個標籤對應。 還有， <span class="codeph"> 影像ID</span> 是刪除副檔名的視頻名稱。 如果該ID的影像不存在，則不顯示海報影像。 </p> <p>要防止顯示預設海報影像，請指定 <span class="codeph"> 無</span> 作為海報影像值。 如果 <span class="codeph"><span class="varname"> 是命令</span></span> 指定，在顯示影像之前，這些命令將應用於預設海報影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

無。

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
