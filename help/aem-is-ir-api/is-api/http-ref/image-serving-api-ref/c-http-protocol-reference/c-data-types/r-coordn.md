---
description: 標準化坐標。 用於指定影像內的相對位置，例如影像偏移或裁切參數，並標準化為影像大小。
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# coordN{#coordn}

標準化坐標。 用於指定影像內的相對位置，例如影像偏移或裁切參數，並標準化為影像大小。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>與影像大小（實數、實數）標準化的坐標偏移 </p></td> 
 </tr> 
</table>

正值會向右下移動。

在許多情況下，參考位置是影像的中心。 在這種情況下，0,0對應於影像的中心，-0.5和-0.5對應於左上角，0.5,0.5對應於右下角。

也可用來指定影像大小或矩形大小，以比較圖層0的大小。 在這種情況下，值必須大於0。 0可能表示應使用特定的預設值。 1,1指定等於圖層0的大小。
