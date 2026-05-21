---
title: opac
description: 不透明度。 指定材質不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
TQID: 'https://experienceleague.adobe.com/j4Y-Lk-BL8VybOYqbP256D81w8FFbQqdS0q8z6Y5l1c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 0%

---

# opac{#opac}

不透明度。 指定材質不透明度。

` opac= *`值`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>材質不透明度（百分比）； 0到100 </p> </td> 
 </tr> 
</table>

下列材質/物件組合支援變數的不透明度：

* 套用至紋理重疊物件的純色和可重複紋理。
* 套用至視窗覆蓋框架物件的視窗覆蓋材料。
* 貼花套用到文字物件或牆物件。

如果材質包含具有Alpha色版的影像，可以使用`opac=`讓影像更透明，但不能更不透明。

## 屬性 {#section-352f7b82ede54159b6afb90ae4b559ec}

材質屬性。 如果目前的物件選取範圍或材料不支援不透明度，則忽略。

## 預設 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`，針對完全不透明的材質（如果影像不包含Alpha色版）。
