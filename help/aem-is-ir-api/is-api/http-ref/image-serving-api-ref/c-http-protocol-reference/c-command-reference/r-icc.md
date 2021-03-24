---
description: 輸出色彩設定檔.
solution: Experience Manager
title: icc
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 4%

---


# icc{#icc}

輸出色彩設定檔.

`icc= *`ObjecttrenderIntentblackpointCompdither`*[, *``*[, *``*[, *``*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 物件</span> </span> </p></td> 
  <td class="stentry"> <p>ICC色彩描述檔。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 感性|相對|飽和度|絕對</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1要啟用，0要禁用黑點補償。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 抖動</span></span> </p></td> 
  <td class="stentry"> <p>1要啟用，0要禁用抖動。 </p></td> 
 </tr> 
</table>

*`object`* 指定如果影像與工作配置檔案不同，應將影像轉換到的輸出顏色空間配置檔案。*`profile`* 必須是在影像目 `icc::Name` 錄或預設目錄的ICC描述檔映射中定義的有效路徑，或是描述檔檔案的相對路徑(通常 [!DNL .icc] 含或 [!DNL .icm] 尾碼)。如需詳細資訊，請參閱[ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

>[!NOTE]
>
>*`object`* 不能包含&#39;,&#39;字元，即使HTTP編碼亦然。

*`renderIntent`* 允許覆蓋預設渲染方式。

*`blackpointComp`* 如果輸出配置檔案支援此功能，則啟用黑點補償。

>[!NOTE]
>
>並非所有色彩轉換都支援所有&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;選項。 通常，僅當ICC輸出配置檔案具有打印機或顯示器等輸出設備的特徵時，才執行這些設定。 此外，某些ICC輸出配置檔案不支援所有&#x200B;*`renderIntent`*&#x200B;選項。

注意

*`dither`* 啟用混色（實際上是誤差擴散），這可避免或減少色帶偽影。

## 屬性 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

請求屬性。 如果指定的映像類型與`fmt=`不匹配，則伺服器將返回錯誤。*`profile`*

*`renderIntent`* 和 *`blackpointComp`* 如果與指定的ICC配置檔案不相容，則忽略。CMYK輸出裝置描述檔更可能支援不同的轉換方式。

## 預設 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

如果已啟用色彩管理且未指定`icc=`，伺服器會傳送轉換為與`fmt=`指定之影像類型相符之輸出描述檔(`attribute::IccProfile*`)的影像。

如果未指定，則&#x200B;*`renderIntent`*&#x200B;繼承自`attribute::IccRenderIntent`,*`blackpointComp`*&#x200B;繼承自`attribute::IccBlackPointCompensation`,*`dither`*&#x200B;繼承自`attribute::IccDither`。

## 另請參閱 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[屬性：:IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ，屬性：:IccRenderPointPoint [，屬性：:IccBlackPointPoint](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，屬性 [：屬性：IccDitherDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) [=ObjectObjectManagementColorIccICCembed,Combed:=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
