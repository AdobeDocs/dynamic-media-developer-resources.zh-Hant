---
title: 標幟
description: 套用旗標。 指定其他演算選項。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
TQID: 'https://experienceleague.adobe.com/tdbtQIxutlPSPRm4vGWCQLM8veyivWfabKos9YbvfYg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 4%

---

# 標幟 {#flags}

套用旗標。 指定其他演算選項。

`flags= *`值`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>標幟值。 </p></td> 
 </tr> 
</table>

目前僅用於機櫃材料。

`flags=0` （預設）呈現帶有實心門的上方機櫃。

`flags=1`呈現上方的玻璃門（如果暈映是由玻璃門所創作）。

## 屬性 {#section-a2b00d7bb15e449ea85178acb92d8285}

材質屬性。 若不是機櫃材料，或目標機櫃物件不允許玻璃門，則忽略此項。

## 預設 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0`無玻璃門。
