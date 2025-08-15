---
title: icc
description: 輸出色彩設定檔。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# icc{#icc}

輸出色彩設定檔。

`icc= *`物件`*[, *`renderIntent`*[, *`blackpointComp`*[, *`dither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">物件</span> </span> </p></td> 
  <td class="stentry"> <p>ICC色彩設定檔。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">感應式|相對|飽和度|絕對</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1代表啟用，0代表停用黑點補償。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">遞色</span></span> </p></td> 
  <td class="stentry"> <p>1代表啟用，0代表停用遞色。 </p></td> 
 </tr> 
</table>

值&#x200B;*`object`*&#x200B;指定影像與工作設定檔不同時應轉換的輸出色域設定檔。 值&#x200B;*`profile`*&#x200B;必須是定義於影像目錄或預設目錄之ICC設定檔對應中的有效`icc::Name`，或是設定檔檔案的相對路徑（通常有[!DNL .icc]或[!DNL .icm]尾碼）。 如需其他資訊，請參閱[*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

>[!NOTE]
>
>值&#x200B;*`object`*&#x200B;可能不包含&#39;，&#39;字元，即使是HTTP編碼亦然。

值&#x200B;*`renderIntent`*&#x200B;允許覆寫預設的演算色彩比對方式。

如果輸出設定檔支援此功能，值&#x200B;*`blackpointComp`*&#x200B;會啟用黑點補償。

>[!NOTE]
>
>並非所有的色彩轉換都支援所有&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;選擇。 通常，這些設定僅在ICC輸出設定檔為輸出裝置（例如印表機或顯示器）的特性時採用。 此外，有些ICC輸出設定檔不支援所有&#x200B;*`renderIntent`*&#x200B;選項。

注意

修飾元&#x200B;*`dither`*&#x200B;會啟用遞色（實際上是誤差擴散），以避免或減少色階誤差。

## 屬性 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

要求屬性。 如果以`fmt=`指定的影像型別不符合&#x200B;*`profile`*，伺服器會傳回錯誤。

若與指定的ICC設定檔不相容，則會忽略修飾元&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*。 CMYK輸出裝置設定檔較有可能支援不同的演算意圖。

## 預設 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

如果已啟用色彩管理且未指定`icc=`，則伺服器會將轉換的影像傳送至與`attribute::IccProfile*`所指定之影像型別相符的輸出設定檔( `fmt=`)。

如果未指定，*`renderIntent`*&#x200B;繼承自`attribute::IccRenderIntent`，*`blackpointComp`*&#x200B;繼承自`attribute::IccBlackPointCompensation`，而&#x200B;*`dither`*&#x200B;繼承自`attribute::IccDither`。

## 另請參閱 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute：：IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，[attribute：：IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)，[attribute：：IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)，[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)，[物件](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)，[色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)，[ICC設定檔對應參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)，[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
