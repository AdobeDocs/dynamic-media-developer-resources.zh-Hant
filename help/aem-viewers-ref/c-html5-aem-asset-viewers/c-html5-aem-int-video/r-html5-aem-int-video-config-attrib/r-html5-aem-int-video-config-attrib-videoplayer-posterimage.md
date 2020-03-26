---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: VideoPlayer.postemage
solution: Experience Manager
title: VideoPlayer.postemage
topic: Dynamic media
uuid: 6b21179c-a227-4194-8640-0fcf73ee80e9
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.postemage{#videoplayer-posterimage}

互動式視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 要在視訊開始播放前顯示在第一個畫格上的影像，已針對伺服器url <span class="codeph"> 解析</span>。 如果在URL中指定，HTTP-encode如下： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 作為 <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>如果 <span class="codeph"><span class="varname"> image_id值被省略</span></span> ，元件會嘗試改用該資產的預設海報影像。 </p> <p>當視訊指定為路徑時，預設海報影像目錄ID會從視訊路徑衍生為 <span class="codeph"> catalog_id/image_id</span> pair，其中catalog_id <span class="codeph"> 對應路徑中的第一個Token,</span> image_id <span class="codeph"></span> 是移除副檔名的視訊名稱。 如果該ID的影像不存在，則不會顯示海報影像。 </p> <p>若要防止顯示預設海報影像，請將 <span class="codeph"> none</span> 指定為海報影像值。 如果僅指 <span class="codeph"><span class="varname"> 定isCommands</span></span> ，則在顯示影像之前，指令會套用至預設海報影像。 </p> </td> 
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

