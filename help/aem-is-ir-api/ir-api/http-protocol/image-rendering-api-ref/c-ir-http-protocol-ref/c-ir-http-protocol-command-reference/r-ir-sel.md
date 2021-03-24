---
description: 依像素位置選取物件。
solution: Experience Manager
title: 選取
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# sel{#sel}

依像素位置選取物件。

` sel= *`木`*, *``*[, *`層`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y  </span> </p> </td> 
  <td class="stentry"> <p>選擇位置坐標（以像素為單位，int、int）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 層級 </span> </p> </td> 
  <td class="stentry"> <p>群組層級(int)。 </p> </td> 
 </tr> 
</table>

在&#x200B;*`x, y`*&#x200B;指定的像素坐標處選擇組或對象，並啟動新的MSS。 如果選擇位置沒有可選對象，或者如果選擇位置無效，則會執行`attribute::OnFailSel`指定的操作。

*`level`* 指定是選擇最外層的組，還是下鑽到嵌套組或對象。如果未指定&#x200B;*`level`*，則會選擇最外層的組。 設定為1可選擇最外層組下方的一個組級別。 設為大數（例如99）以選擇最內層的可選對象或組。

## 屬性 {#section-8f27e84d88734a62a5e398e0c9972bdc}

選取命令；MSS分隔字元。 對象選擇是持續的，直到選擇了另一個對象（具有`obj=`或`sel=`）。

*`x, y`* 必須在0、0（影像左上角）到 *`wid`*-1、 *`hei`*-1（影像的右下角）的範圍內，其中 *`wid`* 和 *`hei`* 是未縮放暈映檢視的大小。

如果指定，*`level`*&#x200B;必須為0或更大。

## 預設 {#section-e13c705a3e76468894b4ec190ed8a893}

*`x, y`*&#x200B;為無。 *`level`* 預設為0。

## 另請參閱 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) wid= [, hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)，屬性：:DefaultPix [，屬](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478) [](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) [性：:On FailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
