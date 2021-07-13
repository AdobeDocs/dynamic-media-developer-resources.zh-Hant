---
description: 按像素位置選擇對象。
solution: Experience Manager
title: 傳送
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# 傳送{#sel}

按像素位置選擇對象。

` sel= *``*, *``*[, *`xylevel`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y  </span> </p> </td> 
  <td class="stentry"> <p>選擇位置坐標（像素，整）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 層級 </span> </p> </td> 
  <td class="stentry"> <p>組級別（整）。 </p> </td> 
 </tr> 
</table>

在&#x200B;*`x, y`*&#x200B;指定的像素坐標處選擇組或對象，並啟動新的MSS。 如果挑庫位置沒有可選對象，或者挑庫位置無效，則執行`attribute::OnFailSel`指定的操作。

*`level`* 指定是選擇最外層的組，還是下鑽到嵌套的組或對象。如果未指定&#x200B;*`level`*，則選擇最外面的組。 設為1可在最外層的組下方選擇一個組級別。 設定為大數（例如99）以選擇最裡面的可選對象或組。

## 屬性 {#section-8f27e84d88734a62a5e398e0c9972bdc}

選擇命令；MSS分隔字元。 對象選擇是持續的，直到選擇了另一個對象（具有`obj=`或`sel=`）。

*`x, y`* 必須在0、0（影像的左上角）到–1、 *`wid`*-1(影 *`hei`*&#x200B;像的右下角)的範圍內，其中和是未縮 *`wid`* 放暈 *`hei`* 映視圖的大小。

如果指定，*`level`*&#x200B;必須為0或更大。

## 預設 {#section-e13c705a3e76468894b4ec190ed8a893}

*`x, y`*&#x200B;無。 *`level`* 預設為0。

## 另請參閱 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
