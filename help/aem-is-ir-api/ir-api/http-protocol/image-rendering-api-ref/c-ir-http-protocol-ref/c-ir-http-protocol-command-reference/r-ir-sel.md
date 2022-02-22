---
title: 選取
description: 按像素位置選擇對象。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# 選取{#sel}

按像素位置選擇對象。

` sel= *`x`*, *`y`*[, *`級別`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>選取位置坐標(以像素為單位(int、int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 層級 </span> </p> </td> 
  <td class="stentry"> <p>組級別(int)。 </p> </td> 
 </tr> 
</table>

在指定的像素坐標處選擇組或對象 *`x, y`* 啟動新的MSS。 如果挑庫位置沒有可選對象，或者如果挑庫位置無效，則由 `attribute::OnFailSel` 的下界。

*`level`* 指定是選擇最外面的組，還是向下鑽取到嵌套組或對象。 如果 *`level`* 未指定，則選擇最外的組。 設定為1以選擇最外層組下的一個組級別。 設定為大數（如99）以選擇最裡面的可選對象或組。

## 屬性 {#section-8f27e84d88734a62a5e398e0c9972bdc}

選擇命令；MSS分隔符。 對象選擇是永久的，直到選擇了另一個對象， `obj=` 或 `sel=`。

*`x, y`* 必須在0、0（影像左上角）到 *`wid`*-1, *`hei`*-1（影像的右下角），其中 *`wid`* 和 *`hei`* 是未縮放視圖的大小。

如果指定， *`level`* 必須為0或更大。

## 預設 {#section-e13c705a3e76468894b4ec190ed8a893}

無 *`x, y`*。 *`level`* 預設為0。

## 另請參閱 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) 。 [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)。 [黑=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)。 [屬性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)。 [屬性：:OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
