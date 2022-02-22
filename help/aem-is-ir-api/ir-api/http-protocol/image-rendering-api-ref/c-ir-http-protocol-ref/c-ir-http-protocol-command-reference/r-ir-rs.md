---
title: rs
description: 高級呈現設定。 指定呈現當前選區時要應用的高級呈現設定。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---

# rs{#rs}

高級呈現設定。 指定呈現當前選區時要應用的高級呈現設定。

`rs= *`谷`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 谷</span> </p> </td> 
  <td class="stentry"> <p>呈現設定字串。 </p></td> 
 </tr> 
</table>

用於微調渲染外觀。 要建立渲染設定字串，請使用Vignette創作工具(Dynamic Media影像創作包的一部分)的渲染功能。

## 屬性 {#section-9a2b2228789046658cb80eddf343af75}

物料屬性。

## 預設 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 範例 {#section-47e4811882574441a4d517e42a35f352}

在影像創作中進行了一些實驗後，確定了反銳化掩模(USM)為給定的應用和材料提供了正確的銳化量。 將配置USM的呈現設定字串複製到 `rs=` 命令與此材料一起使用：

`…&rs=U2V20W50X2&…`

## 另請參閱 {#section-930116e735024a008c994547ba36ee40}

[目錄：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
