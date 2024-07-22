---
title: 選取
description: 依畫素位置選取物件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 1%

---

# 選取{#sel}

依畫素位置選取物件。

` sel= *`x`*, *`y`*[, *`層級`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x，y </span> </p> </td> 
  <td class="stentry"> <p>挑選以畫素(int、int)為單位的位置座標。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">層級</span> </p> </td> 
  <td class="stentry"> <p>群組層級(int)。 </p> </td> 
 </tr> 
</table>

在&#x200B;*`x, y`*&#x200B;指定的畫素座標上選取群組或物件，並開始新的MSS。 如果挑選位置沒有可選取的物件，或挑選位置無效，則會採取`attribute::OnFailSel`指定的動作。

*`level`*&#x200B;指定是否選取最外層的群組，或向下展開至巢狀群組或物件。 如果未指定&#x200B;*`level`*，則會選取最外層的群組。 設為1可選取最外層群組下方的一個群組層級。 設定為大數（例如99）可選取最內層的可選取物件或群組。

## 屬性 {#section-8f27e84d88734a62a5e398e0c9972bdc}

選取範圍指令；MSS分隔符號。 物件選取項會持續存在，直到選取其他物件為止（使用`obj=`或`sel=`）。

*`x, y`*&#x200B;必須在0， 0 （影像的左上角）到&#x200B;*`wid`*-1， *`hei`*-1 （影像的右下角）的範圍內，其中&#x200B;*`wid`*&#x200B;和&#x200B;*`hei`*&#x200B;是未縮放暈映檢視的大小。

若指定，*`level`*&#x200B;必須大於或等於0。

## 預設 {#section-e13c705a3e76468894b4ec190ed8a893}

*`x, y`*&#x200B;沒有專案。 *`level`*&#x200B;預設為0。

## 另請參閱 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ， [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)， [attribute：：DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)， [attribute：：OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
