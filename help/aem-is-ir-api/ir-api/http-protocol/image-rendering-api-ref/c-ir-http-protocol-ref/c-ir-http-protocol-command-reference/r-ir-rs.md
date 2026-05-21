---
title: rs
description: 進階演算設定。 指定呈現目前選取範圍時要套用的進階演算設定。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
TQID: 'https://experienceleague.adobe.com/-wOy--XUu7TX6-rwrUFpuqz82bOwb4wpA9Pa0pM8J-4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# rs{#rs}

進階演算設定。 指定呈現目前選取範圍時要套用的進階演算設定。

`rs= *`值`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>演算設定字串。 </p></td> 
 </tr> 
</table>

用於微調演算外觀。 若要建立演算設定字串，請使用暈映製作工具的演算功能（Dynamic Media影像製作套件的一部分）。

## 屬性 {#section-9a2b2228789046658cb80eddf343af75}

材質屬性。

## 預設 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 範例 {#section-47e4811882574441a4d517e42a35f352}

在「影像製作」中做了一些實驗後，我們判斷不銳利化遮色片(USM)為指定的應用程式和材質提供了正確的銳利化量。 設定USM的轉譯器設定字串會複製到`rs=`命令，以便與下列材料搭配使用：

`…&rs=U2V20W50X2&…`

## 另請參閱 {#section-930116e735024a008c994547ba36ee40}

[catalog：：RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
