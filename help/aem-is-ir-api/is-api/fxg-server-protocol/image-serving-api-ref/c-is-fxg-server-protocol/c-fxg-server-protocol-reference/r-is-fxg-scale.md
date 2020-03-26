---
description: 縮放影像。 相對於全解析度影像，依比例縮放影像。
seo-description: 縮放影像。 相對於全解析度影像，依比例縮放影像。
seo-title: scale
solution: Experience Manager
title: scale
topic: Scene7 Image Serving - Image Rendering API
uuid: db5bab94-e5c1-41fe-ab1b-5c62b6a798d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scale{#scale}

縮放影像。 相對於全解析度影像，依比例縮放影像。

`scale= *`因子`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 因子</span></span> </p> </td> 
  <td class="stentry"> <p>比例系數（實數，&gt;0）。 </p></td> 
 </tr> 
</table>

## 預設 {#section-e9e53959b35844579f0f1d7721b71f8e}

如果未指定，則不使用縮放來使用影像。

## 範例 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
