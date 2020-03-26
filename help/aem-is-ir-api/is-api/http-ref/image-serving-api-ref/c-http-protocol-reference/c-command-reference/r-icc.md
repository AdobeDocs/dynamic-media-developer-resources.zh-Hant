---
description: 輸出色彩設定檔.
seo-description: 輸出色彩設定檔.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

輸出色彩設定檔.

`icc= *`ObjecttrenderIntentblackpointCompdither`*[, *``*[, *``*[, *``*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 物件</span></span> </p></td> 
  <td class="stentry"> <p>ICC色彩描述檔。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> renderIntent <span class="varname"> （演算方式）</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 感性|相對|飽和度|絕對</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1要啟用，0要禁用黑點補償。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 混色</span></span> </p></td> 
  <td class="stentry"> <p>1要啟用，0要禁用抖動。 </p></td> 
 </tr> 
</table>

*`object`* 指定如果影像與工作配置檔案不同，應將影像轉換到的輸出顏色空間配置檔案。 *`profile`* 必須是影像目錄 `icc::Name` 或預設目錄的ICC描述檔映射中定義的有效路徑，或是描述檔檔案的相對路徑(通常具有 [!DNL .icc] 或 [!DNL .icm] 尾碼)。 See [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)for additional information.

>[!NOTE]
>
>*`object`* 不能包含&#39;,&#39;字元，即使HTTP編碼亦然。

*`renderIntent`* 允許覆蓋預設渲染方式。

*`blackpointComp`* 如果輸出配置檔案支援此功能，則啟用黑點補償。

>[!NOTE]
>
>並非所有顏色轉換都支援所 *`renderIntent`* 有 *`blackpointComp`* 選擇。 通常，僅當ICC輸出配置檔案具有打印機或顯示器等輸出設備的特徵時，才執行這些設定。 此外，有些ICC輸出設定檔不支援所有 *`renderIntent`* 選項。

注意

*`dither`* 啟用混色（實際上是誤差擴散），這可避免或減少色帶偽影。

## 屬性 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

請求屬性。 如果指定的影像類型不符合，則伺服器 `fmt=` 會傳回錯誤 *`profile`*。

*`renderIntent`* 和 *`blackpointComp`* 如果與指定的ICC配置檔案不相容，則忽略。 CMYK輸出裝置描述檔更可能支援不同的轉換方式。

## 預設 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

如果已啟用色彩管 `icc=` 理且未指定，伺服器會傳送轉換為輸出描述檔( `attribute::IccProfile*`)的影像，以符合指定的影像類型 `fmt=`。

如果未指定， *`renderIntent`* 則從中繼 `attribute::IccRenderIntent`承 *`blackpointComp`* 、從中繼承 `attribute::IccBlackPointCompensation`, *`dither`* 並從中繼承 `attribute::IccDither`。

## 另請參閱 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[屬性：IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ，屬性：:IccRenderPointPoint [，屬性：:IccRenderAttribute](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f):IccDitherDither [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[=HobjectObjectManagementColorIccICCEmbed,CombeddidembedMap=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
