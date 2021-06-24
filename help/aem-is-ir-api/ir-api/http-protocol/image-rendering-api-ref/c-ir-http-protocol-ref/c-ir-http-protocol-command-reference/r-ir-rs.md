---
description: 進階演算設定。 指定在呈現當前選區時應用的高級渲染設定。
solution: Experience Manager
title: rs
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# rs{#rs}

進階演算設定。 指定在呈現當前選區時應用的高級渲染設定。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>呈現設定字串。 </p></td> 
 </tr> 
</table>

用於微調渲染外觀。 使用暈映製作工具(Dynamic Media影像製作套件的一部分)的轉譯功能，建立轉譯設定字串。

## 屬性 {#section-9a2b2228789046658cb80eddf343af75}

材料屬性。

## 預設 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 範例 {#section-47e4811882574441a4d517e42a35f352}

在影像製作中進行一些實驗之後，確定非銳利化遮色片(USM)可為指定的應用程式和材料提供正確的銳利化量。 配置USM的呈現設定字串被複製到`rs=`命令以與以下材料一起使用：

`…&rs=U2V20W50X2&…`

## 另請參閱 {#section-930116e735024a008c994547ba36ee40}

[目錄：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
