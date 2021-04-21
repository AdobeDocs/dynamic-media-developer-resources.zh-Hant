---
description: 進階演算設定。 指定在渲染當前選區時要應用的高級渲染設定。
solution: Experience Manager
title: rs
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# rs{#rs}

進階演算設定。 指定在渲染當前選區時要應用的高級渲染設定。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>演算設定字串。 </p></td> 
 </tr> 
</table>

用於微調渲染外觀。 使用暈映製作工具(Dynamic Media影像製作套件的一部分)的演算功能來建立演算設定字串。

## 屬性 {#section-9a2b2228789046658cb80eddf343af75}

材料屬性。

## 預設 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 範例 {#section-47e4811882574441a4d517e42a35f352}

在「影像製作」中進行一些實驗後，確定非銳利化遮色片(USM)可為特定應用程式和材質提供正確銳利化量。 配置USM的渲染設定字串被複製到`rs=`命令中，以便與以下內容一起使用：

`…&rs=U2V20W50X2&…`

## 另請參閱 {#section-930116e735024a008c994547ba36ee40}

[目錄：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
