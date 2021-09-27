---
title: VideoPlayer.posterimage
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 17c1220d-f2a4-4729-84e2-b9f6f5732423
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

互動式視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 要在視訊開始播放前顯示在第一個畫面上的影像，針對<span class="codeph">伺服器url</span>解析。 若在URL中指定，請以HTTP編碼： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 作為 <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> </span> as  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>如果省略<span class="codeph"><span class="varname"> image_id</span></span>值，元件會嘗試為該資產使用預設海報影像。 </p> <p>當視訊指定為路徑時，預設海報影像目錄ID從視訊路徑衍生為<span class="codeph"> catalog_id/image_id</span>對，其中<span class="codeph"> catalog_id</span>對應於路徑中的第一個代號。 且， <span class="codeph"> image_id</span>是已移除副檔名的視訊名稱。 如果具有該ID的影像不存在，則不會顯示海報影像。 </p> <p>若要防止顯示預設海報影像，請指定<span class="codeph"> none</span>作為海報影像值。 如果僅指定<span class="codeph"><span class="varname"> isCommands</span></span> ，則在顯示影像之前，這些命令將應用於預設海報影像。 </p> </td> 
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
