---
title: 標幟
description: 應用標誌。 指定其他呈現選項。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 5%

---

# 標幟 {#flags}

應用標誌。 指定其他呈現選項。

`flags= *`谷`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 谷</span> </p> </td> 
  <td class="stentry"> <p>標誌值。 </p></td> 
 </tr> 
</table>

當前僅用於機櫃材料。

`flags=0` （預設）呈現帶實體門的上機櫃。

`flags=1` 呈現帶玻璃門的上機櫃（如果創作者是帶玻璃門的）。

## 屬性 {#section-a2b00d7bb15e449ea85178acb92d8285}

物料屬性。 如果不是機櫃材料，或目標機櫃對象不允許玻璃門，則忽略。

## 預設 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 沒有玻璃門。
