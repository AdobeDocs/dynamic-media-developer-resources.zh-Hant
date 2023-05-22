---
description: 歸一化坐標。 用於指定影像內的相對位置，如影像偏移或裁剪參數，這些位置與影像大小歸一化。
solution: Experience Manager
title: 坐標N
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 坐標N{#coordn}

歸一化坐標。 用於指定影像內的相對位置，如影像偏移或裁剪參數，這些位置與影像大小歸一化。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐標N</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>。 <span class="codeph"><span class="varname"> 無</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>。 <span class="codeph"><span class="varname"> 無</span></span> </p></td> 
  <td class="stentry"> <p>歸一化為影像大小（實數、實數）的坐標偏移 </p></td> 
 </tr> 
</table>

正值向右下移動。

在許多情況下，參考位置是影像的中心。 在這種情況下，0,0對應於影像的中心，-0.5,-0.5對應於左上角，0.5,0.5對應於右下角。

還用於指定影像大小或相對於圖層0的矩形大小。 在這種情況下，值必須大於0。 0可能表示應使用特定預設值。 1,1指定與層0的大小相等的大小。
