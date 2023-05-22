---
description: 輸出色彩設定檔.
solution: Experience Manager
title: icc
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 3%

---

# icc{#icc}

輸出色彩設定檔.

`icc= *`對象`*[, *`呈現意圖`*[, *`黑點元件`*[, *`抖動`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 對象</span> </span> </p></td> 
  <td class="stentry"> <p>ICC顏色配置檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 呈現意圖</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 感知|相對|飽和度|絕對</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 黑點元件</span></span> </p></td> 
  <td class="stentry"> <p>1要啟用，0要禁用黑點補償。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 抖動</span></span> </p></td> 
  <td class="stentry"> <p>啟用1，禁用抖動0。 </p></td> 
 </tr> 
</table>

*`object`* 指定影像與工作配置檔案不同時應轉換到的輸出顏色空間配置檔案。 *`profile`* 必須有效 `icc::Name` 在映像目錄或預設目錄的ICC配置檔案映射中定義，或在配置檔案的相對路徑中定義(通常與 [!DNL .icc] 或 [!DNL .icm] 尾碼)。 請參閱 [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)的雙曲餘切值。

>[!NOTE]
>
>*`object`* 不能包含「，」字元，即使HTTP編碼。

*`renderIntent`* 允許覆蓋預設渲染方法。

*`blackpointComp`* 如果輸出配置檔案支援此功能，則啟用黑點補償。

>[!NOTE]
>
>並非所有顏色轉換都支援所有 *`renderIntent`* 和 *`blackpointComp`* 選項。 通常，僅當ICC輸出配置檔案表示輸出設備（如打印機或顯示器）時，才執行這些設定。 此外，某些ICC輸出配置檔案不支援所有 *`renderIntent`* 選項。

注意

*`dither`* 啟用抖動（實際上是誤差擴散），這可能避免或減少色帶偽影。

## 屬性 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

請求屬性。 如果指定的映像類型為 `fmt=` 不匹配 *`profile`*。

*`renderIntent`* 和 *`blackpointComp`* 如果與指定的ICC配置檔案不相容，則忽略。 CMYK輸出設備配置檔案更可能支援不同的渲染方式。

## 預設 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

如果啟用了顏色管理，並 `icc=` 未指定，伺服器將傳送轉換為輸出配置檔案的映像( `attribute::IccProfile*`)與指定的映像類型匹配 `fmt=`。

如果未指定， *`renderIntent`* 繼承自 `attribute::IccRenderIntent`。 *`blackpointComp`* 繼承自 `attribute::IccBlackPointCompensation`, *`dither`* 繼承自 `attribute::IccDither`。

## 另請參閱 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[屬性：:IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) 。 [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)。 [屬性：:IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)。 [屬性：:IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)。 [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)。 [對象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。 [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)。 [ICC配置檔案映射參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)。 [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
