---
title: PageView.zoomstep
description: PageView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *`步`*[, *`限`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步驟</span></span> </p> </td> 
   <td colname="col2"> <p> 配置將解析度提高或降低兩倍所需的放大和縮小操作數。 每個縮放操作的解析度變化是每步2^1。 設定為 <span class="codeph"> 0</span> 以使用單個縮放操作縮放到完全解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相對於全解析度影像的最大縮放解析度。 預設值為 <span class="codeph"> 1.0</span>，這不允許超出全解析度的縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-636d35a4791447039f1902973f568320}

選擇性.

## 預設 {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## 範例 {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
