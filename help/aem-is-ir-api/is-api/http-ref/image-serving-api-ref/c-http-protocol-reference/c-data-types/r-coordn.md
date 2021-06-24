---
description: 標準化坐標。 用於指定影像內的相對位置，例如影像偏移或裁切參數，已標準化為影像大小。
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# coordN{#coordn}

標準化坐標。 用於指定影像內的相對位置，例如影像偏移或裁切參數，已標準化為影像大小。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>，紐 <span class="codeph"><span class="varname"> 約</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>，紐 <span class="codeph"><span class="varname"> 約</span></span> </p></td> 
  <td class="stentry"> <p>已標準化為影像大小的坐標偏移（實、實） </p></td> 
 </tr> 
</table>

正值朝右下方移動。

在許多情況下，參照位置是影像的中心。 在此情況下，0,0對應於影像的中心，-0.5,-0.5對應於左上角，0.5,0.5對應於右下角。

還用於指定影像大小或相對於圖層0的大小的矩形大小。 在此情況下，值必須大於0。 0可表示應使用特定預設值。 1,1指定等於層0的大小。
