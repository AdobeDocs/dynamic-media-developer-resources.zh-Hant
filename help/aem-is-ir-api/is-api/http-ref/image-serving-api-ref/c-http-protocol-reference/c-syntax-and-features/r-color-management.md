---
description: 「影像伺服」支援根據符合ICC（國際色彩協會）規格的色域描述檔進行色域轉換。
solution: Experience Manager
title: 影像伺服色彩管理
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 0%

---


# 影像伺服色彩管理{#image-serving-color-management}

「影像伺服」支援根據符合ICC（國際色彩協會）規格的色域描述檔進行色域轉換。

## 預設色域{#section-8cfe60808bce49968091995e4e521dba}

每個影像目錄（和預設目錄）都可定義一組ICC描述檔，這些描述檔構成此目錄的預設色域——一個輸入描述檔和一個輸出描述檔，每個描述檔分別用於灰階、RGB和CMYK資料。 請參閱` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`、` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`、` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`、` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`、` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`和` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`。

## 輸入色域{#section-9f08e2c1b6aa4fe4815be174972c1944}

源影像可嵌入ICC配置檔案以定義輸入顏色空間。 如果源影像中沒有嵌入配置檔案，則將使用與源影像的像素類型對應的適用影像目錄的`attribute::IccProfileSrc*`。 如果未在映像目錄中定義此屬性，則使用`attribute::IccProfile*`。 如果未定義該目錄屬性，則影像不受色彩管理，只會套用天真的變形。

## 輸出色域{#section-b517bca622b64dcfa7defba6035d0716}

使用`icc=`命令定義請求的最終影像結果的顏色空間。 如果未指定`icc=`，則使用與輸出影像的像素類型相對應的預設輸出顏色空間（來自請求的主目錄）作為輸出顏色空間。 如果未在主目錄或預設目錄中定義輸出描述檔，且如果基底層是內嵌描述檔且符合輸出像素類型的影像，則該描述檔會用於輸出色彩空間。 否則，輸出色域仍未定義——在像素類型之間轉換時，只會套用天真的色彩轉換，而輸出影像中不會內嵌任何色彩描述檔。

嵌套／嵌入式影像服務請求的輸出顏色空間始終與外部嵌入請求的輸出顏色空間相同。

## 純色{#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

如果顏色值包含尾碼&#39;S&#39;，則使用`color=`、`bgcolor=`或RTF命令`\iscolortbl`指定的顏色值將與輸入顏色空間相關聯，否則它們與輸出顏色空間相關聯。 使用`bgc=`或RTF命令`\colortbl`和`\cmykcolortbl`指定的顏色值始終與相應的預設或實際輸出顏色空間相關聯。

>[!NOTE]
>
>目前，`bgc=`未完全參與色彩管理——使用`bgc=`指定時會忽略&#39;S&#39;字尾，當使用`bgc=`指定的色彩值的像素類型與輸出影像的像素類型不同時，會套用天真轉換。 否則，`bgc=`與實際輸出色域相關聯。

## 巢狀和內嵌的請求{#section-bdda638c31504f26a77e51ebb1ea6e3b}

嵌套的IS請求和嵌入的IR請求的輸出顏色空間被自動設定為最外層請求的輸出顏色空間，除非嵌套請求指定具有`icc=`的顯式輸出顏色空間。 此外，巢狀／內嵌請求也會繼承最外層請求主目錄的預設輸出色域，以確保對純色值的處理一致。

## 色域轉換{#section-ca87b80b8e364ea59d8a92d87121b0fb}

影像伺服通常會嘗試在處理期間延遲色彩轉換。 如果影像的所有圖層都有相同的圖層色彩空間，則在合併及最終縮放後，會轉換為輸出色彩空間。 如果涉及多層色域，則在合併之前，將每個層轉換為輸出色域。

>[!NOTE]
>
>命令`op_brightness=`、`op_colorbalance=`、`op_colorize=`、`op_contrast=`、`op_hue=`和`op_saturation=`是RGB操作。 這些操作僅在圖層顏色空間具有RGB像素類型時才會保持顏色的完整性。 如果RGB以外的其他顏色，則使用天真的色彩轉換將資料轉換為RGB，而結果的色彩保真度會有限。 此類圖層的圖層色彩空間應視為不確定。

顏色轉換選項隨`icc=`提供，如果未指定`icc=`，則提供`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`和`attribute::IccDither`。

## 嵌入顏色配置檔案{#section-261ebbae5ce046589a776ca972380052}

可通過指定`iccEmbed=`將輸出色域的ICC顏色配置檔案（如果可用）嵌入到響應影像中。

## 管理ICC配置式{#section-eb210e4b44e64e2c8b80ee59216c5555}

伺服器使用的所有顏色配置檔案都必須符合ICC規範。 ICC配置檔案通常具有[!DNL .icc]或[!DNL .icm]檔案尾碼，並與影像資料檔案共同定位。

雖然輸出配置檔案可以在`icc=`命令中由檔案路徑／名稱指定，但建議在預設目錄或映像目錄的ICC配置檔案映射中註冊所有配置檔案，並使用快捷方式標識符(`icc::Name`)而不是檔案路徑。

`catalog::IccProfile`和`attribute::IccProfile*`中引用的所有ICC配置檔案都必須註冊到映像或預設目錄的ICC配置檔案映射中。

## 限制{#section-fb50ede40b124b89b30679da29782ab5}

目前僅支援CMYK、RGB和灰階色彩空間。

## 包含的ICC色彩描述檔{#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

「影像伺服」在預設影像目錄中包含最標準的AdobeICC描述檔。 這些描述檔可透過其共同名稱(例如，如Photoshop所示)或較短的識別碼來存取。 下表列出所有標準ICC配置檔案。 當使用`icc=`命令中的公用名稱引用配置檔案時，空格必須編碼為`%20`。

其他描述檔可新增至標準描述檔，可新增至預設目錄或特定影像目錄。 有關詳細資訊，請參閱[ICC配置式映射參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)。

>[!NOTE]
>
>下表僅適用於&#x200B;*Dynamic MediaHybrid*（在`dynamicmedia`運行模式下運行）。

|標識符|公用名稱|檔案名|
|— |— |— |
|**RGB**||||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB`|CIE RGB|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC(1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto`|ProPhoto RGB|ProPhoto.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb色域設定檔。icm|
|`WideGamutRGB`|寬色域RGB|WideGamitRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Cobated FOGRA27(ISO 12647-2:2004)|CobatedFOGRA27.icc|
|`CoatedFogra39`|Cobated FOGRA39(ISO 12647-2:2004)|CobatedFOGRA39.icc|
|`CoatedGraCol`|Cobated GRACoL 2006(ISO 12647-2:2004)|CobatedGRACoL2006.icc|
|`EuropeISOCoated`|歐洲ISO塗層FOGRA27|EuropeISOCotatedFOGRA27.icc|
|`EuroscaleCoated`|Euroscale Cobated|EuroscaleCobated.icc|
|`EuroscaleUncoated`|Euroscale Uncoved v2|EuroscaleUncoved.icc|
|`JapanColorCoated`|Japan Color 2001 Covated|JapanColor2001Covated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncovated|JapanColor2001Uncovated.icc|
|`JapanColorWebCoated`|Japan Color 2003 Web Corated|JapanColor2003WebCobated.icc|
|`JapanWebCoated`|Japan Web Cobated(Ad)|JapanWebCobated.icc|
|`NewsprintSNAP2007`|US Newsperint(SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|Photoshop4預設CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop5預設CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|美國Sheetfed Covated v2|USSheetfedCovated.icc|
|`SheetfedUncoated`|USSheetfed Uncoved v2|USSheetfedUncoved.icc|
|`UncoatedFogra29`|未塗覆的FOGRA29(ISO 12647-2:2004)|UncopatedFOGRA29.icc|
|`WebCoated`|USWeb Cobated(SWOP)v2|USWebCobatedSWOP.icc|
|`WebCoatedFogra28`|Web Cobated FOGRA28(ISO 12647-2:2004)|WebCobatedFOGRA28.icc|
|`WebCoatedGrade3`|Web Cobated SWOP 2006 3級紙|WebCobatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Web Cobated SWOP 2006 5級紙|WebCobatedSWOP2006Grade5.icc|
|`WebUncoated`|USWeb Uncovated v2|USWebUncoved.icc|

下表適用於&#x200B;*Dynamic Media經典映像服務*&#x200B;和&#x200B;*Dynamic Media*（在`dynamicmedia_scene7`運行模式下運行）。

|標識符|公用名稱|檔案名|
|— |— |— |
|**RGB**||||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB|CIE RGB`|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC(1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb色域設定檔。icm|
|`WideGamutRGB`|寬色域RGB|WideGamitRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Cobated FOGRA27(ISO 12647-2:2004)|CobatedFOGRA27.icc|
|`CoatedFogra39`|Cobated FOGRA39(ISO 12647-2:2004)|CobatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|Cobated GRACoL 2006(ISO 12647-2:2004)|CobatedGRACoL2006.icc|
|`EuropeISOCoated`|歐洲ISO塗層FOGRA27|EuropeISOCotatedFOGRA27.icc|
|`Euroscale Coated v2`|Euroscale Cobated v2|EuroscaleCobated.icc|
|`EuroscaleUncoated`|Euroscale Uncoved v2|EuroscaleUncoved.icc|
|`JapanColorCoated`|Japan Color 2001 Covated|JapanColor2001Covated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncovated|JapanColor2001Uncovated.icc|
|`Japan Color 2003 Web Coated`|Japan Color 2003 Web Corated|JapanColor2003WebCobated.icc|
|`JapanWebCoated`|Japan Web Cobated(Ad)|JapanWebCobated.icc|
|`PS4Default`|Photoshop4預設CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop5預設CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|美國Sheetfed Covated v2|USSheetfedCovated.icc|
|`SheetfedUncoated`|美國Sheetfed Uncoved v2|USSheetfedUncoved.icc|
|`UncoatedFogra29`|未塗覆的FOGRA29(ISO 12647-2:2004)|UncopatedFOGRA29.icc|
|`US Newsprint (SNAP 2007)`|US Newsperint(SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|USWeb Cobated(SWOP)v2|USWebCobatedSWOP.icc|
|`WebCoatedFogra28`|Web Cobated FOGRA28(ISO 12647-2:2004)|WebCobatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Web Cobated SWOP 2006 3級紙|WebCobatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Web Cobated SWOP 2006 5級紙|WebCobatedSWOP2006Grade5.icc|
|`WebUncoated`|USWeb Uncovated v2|USWebUncoved.icc|

## 另請參閱 {#section-39159397e80b4efca5f631eab8b9aa06}

[國際色彩協會](http://www.color.org/index.xalter), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [Embed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)，屬性：Icc Profile [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) [](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), Icc屬性：ProfileIcc*ProfileIcc屬性：Icc屬性：IccIcc屬性RenderAttribute Attribute:BlackIccBlackIccBedPointCompant，屬性Ic Diter Dithter Iter Ater Atter:ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,ICC,CCCCCC,C,C,CC,C,C,C,C,C,C,C,C,C,C,C,C,C,CR,C,C,CR,CR,CR,CR,CO,CO,CR,CR,CRA,CRA,CR,CR,CR,  [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
