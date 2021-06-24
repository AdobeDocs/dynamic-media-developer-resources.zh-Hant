---
description: 縮放影像。 相對於全解析度影像逐個縮放影像。
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 8%

---

# 比例{#scale}

縮放影像。 相對於全解析度影像逐個縮放影像。

`scale= *`因子`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 因子</span></span> </p> </td> 
  <td class="stentry"> <p>比例因子（實數，&gt;0）。 </p></td> 
 </tr> 
</table>

## 預設 {#section-e9e53959b35844579f0f1d7721b71f8e}

如果未指定，則使用影像時不縮放。

## 範例 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
