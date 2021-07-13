---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: d92e56ae-2bb6-46f6-b0f7-64b867492a37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---

# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *``*[, *`steplimit`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步驟</span></span> </p> </td> 
   <td colname="col2"> <p> 配置需要的放大和縮小操作數，以將解析度增加或減少2倍。 每個縮放動作的解析度變化為每步驟2^1。 設為<span class="codeph"> 0</span> ，只要執行一次縮放動作即可縮放至完整解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相對於完整解析度影像的最大縮放解析度。 預設值為<span class="codeph"> 1.0</span>，不允許縮放超過完全解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-636d35a4791447039f1902973f568320}

選填。

## 預設 {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## 範例 {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
