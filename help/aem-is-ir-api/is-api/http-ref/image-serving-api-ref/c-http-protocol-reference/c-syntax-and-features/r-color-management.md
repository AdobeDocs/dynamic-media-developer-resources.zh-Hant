---
description: 「影像伺服」支援基於符合ICC（國際顏色協會）規範的顏色空間配置檔案的顏色空間轉換。
solution: Experience Manager
title: 影像提供色彩管理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1200'
ht-degree: 0%

---

# 影像提供色彩管理{#image-serving-color-management}

「影像伺服」支援基於符合ICC（國際顏色協會）規範的顏色空間配置檔案的顏色空間轉換。

## 預設色域 {#section-8cfe60808bce49968091995e4e521dba}

每個影像目錄（和預設目錄）都可以定義一組ICC配置檔案，這些配置檔案構成此目錄的預設顏色空間 — 每個輸入和輸出配置檔案分別用於灰度、RGB和CMYK資料。 請參閱` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`、` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`、` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`、` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`、` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`和` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`。

## 輸入色域 {#section-9f08e2c1b6aa4fe4815be174972c1944}

源影像可以嵌入ICC配置檔案以定義輸入顏色空間。 如果源影像中未嵌入任何輪廓，則將使用與源影像的像素類型對應的適用影像目錄的`attribute::IccProfileSrc*`。 如果未在影像目錄中定義此屬性，則使用`attribute::IccProfile*`。 如果該目錄屬性也未定義，則影像不會受色彩管理，而只會套用天真的轉換。

## 輸出色域 {#section-b517bca622b64dcfa7defba6035d0716}

使用`icc=`命令定義請求的最終影像結果的顏色空間。 如果未指定`icc=`，則與輸出影像的像素類型相對應的預設輸出顏色空間（來自請求的主目錄）將用作輸出顏色空間。 如果沒有在主目錄或預設目錄中定義輸出輪廓，並且如果基層是具有與輸出像素類型匹配的嵌入式輪廓的影像，則該輪廓用於輸出顏色空間。 否則，輸出顏色空間仍未定義 — 在像素類型之間轉換時只應用天真的顏色轉換，並且輸出影像中不能嵌入任何顏色配置檔案。

嵌套/嵌入影像服務請求的輸出顏色空間始終與外部嵌入請求的輸出顏色空間相同。

## 純色 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

如果顏色值包含尾碼「S」，則使用`color=`、`bgcolor=`或RTF命令`\iscolortbl`指定的顏色值將與輸入顏色空間相關聯，否則它們與輸出顏色空間相關聯。 使用`bgc=`或RTF命令`\colortbl`和`\cmykcolortbl`指定的顏色值始終與相應的預設或實際輸出顏色空間相關聯。

>[!NOTE]
>
>此時，`bgc=`未完全參與顏色管理 — 當以`bgc=`指定時，將忽略「S」尾碼，當以`bgc=`指定的顏色值的像素類型與輸出影像的像素類型不同時，將應用天真轉換。 否則，`bgc=`與實際輸出顏色空間相關聯。

## 巢狀和內嵌的請求 {#section-bdda638c31504f26a77e51ebb1ea6e3b}

嵌套的IS請求和嵌入的IR請求的輸出顏色空間自動設定為最外層請求的輸出顏色空間，除非嵌套請求指定了具有`icc=`的顯式輸出顏色空間。 此外，巢狀/內嵌請求也會繼承最外層請求之主要目錄的預設輸出色彩空格，以確保實色值的處理一致。

## 色域轉換 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

「影像伺服」一般會嘗試在處理期間延遲顏色轉換。 如果影像的所有圖層都具有相同的圖層顏色空間，則在合併並最終縮放後，將顏色空間轉換為輸出顏色空間。 如果涉及多個層顏色空間，則在合併之前將每個層轉換為輸出顏色空間。

>[!NOTE]
>
>命令`op_brightness=`、`op_colorbalance=`、`op_colorize=`、`op_contrast=`、`op_hue=`和`op_saturation=`為RGB操作。 這些操作僅在圖層顏色空間具有RGB像素類型時才保持顏色保真度。 如果RGB以外，則資料會使用天真顏色轉換來轉換為RGB，結果的色彩保真度將有限。 應將此類層的層顏色空間視為不確定。

顏色轉換選項是隨`icc=`提供的，或者，如果未指定`icc=`，則使用`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`和`attribute::IccDither`。

## 內嵌顏色描述檔 {#section-261ebbae5ce046589a776ca972380052}

可通過指定`iccEmbed=`將輸出顏色空間的ICC顏色配置檔案嵌入到響應影像中（如果可用）。

## 管理ICC配置檔案 {#section-eb210e4b44e64e2c8b80ee59216c5555}

伺服器使用的所有顏色配置檔案都必須符合ICC規範。 ICC配置檔案通常具有[!DNL .icc]或[!DNL .icm]檔案尾碼，並與影像資料檔案共用。

雖然可以在`icc=`命令中由檔案路徑/名稱指定輸出配置檔案，但建議在預設目錄或影像目錄的ICC配置檔案映射中註冊所有配置檔案，並使用快捷方式標識符(`icc::Name`)，而不是檔案路徑。

`catalog::IccProfile`和`attribute::IccProfile*`中引用的所有ICC配置檔案都必須註冊到影像或預設目錄的ICC配置檔案映射中。

## 限制 {#section-fb50ede40b124b89b30679da29782ab5}

目前僅支援CMYK、RGB和灰階色域。

## 包含的ICC顏色配置檔案 {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

「影像伺服」在預設影像目錄中包含大部分標準AdobeICC設定檔。 這些設定檔可透過其共同名稱(例如，如Photoshop中所示)或較短的識別碼來存取。 下表列出所有標準ICC配置檔案。 當使用`icc=`命令的公共名稱引用配置檔案時，必須將空格編碼為`%20`。

可將其他設定檔新增至標準設定檔，可新增至預設目錄或特定影像目錄。 有關詳細資訊，請參閱[ICC配置檔案映射參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)。

>[!NOTE]
>
>下表僅適用於&#x200B;*Dynamic Media Hybrid*（在`dynamicmedia`執行模式中執行）。

|標識符|公用名|檔案名|
| — | — | — |
|**RGB**|||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB`|CIE RGB|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC(1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto`|ProPhoto RGB|ProPhoto.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb色彩空間Profile.icm|
|`WideGamutRGB`|寬色域RGB|WideGamotRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Cobated FOGRA27(ISO 12647-2:2004)|CobatedFOGRA27.icc|
|`CoatedFogra39`|Cobated FOGRA39(ISO 12647-2:2004)|CobatedFOGRA39.icc|
|`CoatedGraCol`|Cobated GRACoL 2006(ISO 12647-2:2004)|CobatedGRACoL2006.icc|
|`EuropeISOCoated`|歐洲ISO塗層FOGRA27|EuropeISOCotaedFOGRA27.icc|
|`EuroscaleCoated`|Euroscale Cobated|EuroscaleCobated.icc|
|`EuroscaleUncoated`|Euroscale Uncobated v2|EuroscaleUncobated.icc|
|`JapanColorCoated`|Japan Color 2001 Cobated|JapanColor2001Cobated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Appent|JapanColor2002Eppane.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncobated|JapanColor2001Uncobated.icc|
|`JapanColorWebCoated`|Japan Color 2003 Web Cobated|JapanColor2003WebCobated.icc|
|`JapanWebCoated`|Japan Web Cobated(Ad)|JapanWebCobated.icc|
|`NewsprintSNAP2007`|US Newsprint(SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|Photoshop 4預設CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5預設CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|US張紙塗布v2|USSheetfedCobated.icc|
|`SheetfedUncoated`|US張紙未塗覆v2|USSheetfedUncobated.icc|
|`UncoatedFogra29`|未塗覆的FOGRA29(ISO 12647-2:2004)|未塗覆的FOGRA29.icc|
|`WebCoated`|USWeb Cobated(SWOP)v2|USWebCobatedSWOP.icc|
|`WebCoatedFogra28`|Web Cobated FOGRA28(ISO 12647-2:2004)|WebCobatedFOGRA28.icc|
|`WebCoatedGrade3`|Web Cobated SWOP 2006 3級紙|WebCobatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Web Cobated SWOP 2006第5級紙|WebCobatedSWOP2006Grade5.icc|
|`WebUncoated`|USWeb Uncobated v2|USWebUncobated.icc|

下表適用於&#x200B;*Dynamic Media Classic Image Serving*&#x200B;和&#x200B;*Dynamic Media*（以`dynamicmedia_scene7`執行模式執行）。

|標識符|公用名|檔案名|
| — | — | — |
|**RGB**|||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB|CIE RGB`|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC(1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb色彩空間Profile.icm|
|`WideGamutRGB`|寬色域RGB|WideGamotRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Cobated FOGRA27(ISO 12647-2:2004)|CobatedFOGRA27.icc|
|`CoatedFogra39`|Cobated FOGRA39(ISO 12647-2:2004)|CobatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|Cobated GRACoL 2006(ISO 12647-2:2004)|CobatedGRACoL2006.icc|
|`EuropeISOCoated`|歐洲ISO塗層FOGRA27|EuropeISOCotaedFOGRA27.icc|
|`Euroscale Coated v2`|Euroscale Cobated v2|EuroscaleCobated.icc|
|`EuroscaleUncoated`|Euroscale Uncobated v2|EuroscaleUncobated.icc|
|`JapanColorCoated`|Japan Color 2001 Cobated|JapanColor2001Cobated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Appent|JapanColor2002Eppane.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncobated|JapanColor2001Uncobated.icc|
|`Japan Color 2003 Web Coated`|Japan Color 2003 Web Cobated|JapanColor2003WebCobated.icc|
|`JapanWebCoated`|Japan Web Cobated(Ad)|JapanWebCobated.icc|
|`PS4Default`|Photoshop 4預設CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5預設CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|US張紙塗布v2|USSheetfedCobated.icc|
|`SheetfedUncoated`|US張紙未塗覆v2|USSheetfedUncobated.icc|
|`UncoatedFogra29`|未塗覆的FOGRA29(ISO 12647-2:2004)|未塗覆的FOGRA29.icc|
|`US Newsprint (SNAP 2007)`|US Newsprint(SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|USWeb Cobated(SWOP)v2|USWebCobatedSWOP.icc|
|`WebCoatedFogra28`|Web Cobated FOGRA28(ISO 12647-2:2004)|WebCobatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Web Cobated SWOP 2006 3級紙|WebCobatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Web Cobated SWOP 2006第5級紙|WebCobatedSWOP2006Grade5.icc|
|`WebUncoated`|USWeb Uncobated v2|USWebUncobated.icc|

## 另請參閱 {#section-39159397e80b4efca5f631eab8b9aa06}

[國際顏色聯盟](http://www.color.org/index.xalter),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*,  [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccBlackPointCompentation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c),  [, ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)color= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)bgc=,  [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
