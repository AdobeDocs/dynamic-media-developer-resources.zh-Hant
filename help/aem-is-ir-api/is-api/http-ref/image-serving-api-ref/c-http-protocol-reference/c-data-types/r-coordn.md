---
title: coordN
description: 標準化座標。 用於指定影像內的相對位置，例如影像位移或裁切引數，標準化為影像的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
TQID: 'https://experienceleague.adobe.com/-dtYByOGK-mNAWc0yQBs4nu5sO1r-Ormq70iwdDZBjg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 0%

---

# coordN{#coordn}

標準化座標。 用於指定影像內的相對位置，例如影像位移或裁切引數，標準化為影像的大小。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>，<span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>，<span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>將座標位移標準化為影像大小（實數、實數） </p></td> 
 </tr> 
</table>

正值會向右下方移動。

通常，參照位置是影像的中心。 在此案例中，`0,0`對應至影像中心，`-0.5,-0.5`對應至左上角，`0.5,0.5`對應至右下角。

它也可以用來指定影像大小或相對於圖層0大小的矩形大小。 在此情況下，值必須大於0。 0表示應使用特定的預設值。 值`1,1`指定等於圖層0的大小。
