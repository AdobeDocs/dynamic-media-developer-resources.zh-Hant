---
description: 影像服務支援基於符合ICC（國際顏色聯盟）規範的顏色空間配置檔案的顏色空間轉換。
solution: Experience Manager
title: 影像服務顏色管理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# 影像服務顏色管理{#image-serving-color-management}

影像服務支援基於符合ICC（國際顏色聯盟）規範的顏色空間配置檔案的顏色空間轉換。

## 預設顏色空格 {#section-8cfe60808bce49968091995e4e521dba}

每個影像目錄（和預設目錄）都可以定義一組ICC配置檔案，這些配置檔案構成了此目錄的預設顏色空間 — 每個輸入配置檔案和一個輸出配置檔案用於灰度、RGB和CMYK資料。 請參閱 ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`。 ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`。 ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`。 ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`。 ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`, ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`。

## 輸入顏色空間 {#section-9f08e2c1b6aa4fe4815be174972c1944}

源影像可以嵌入ICC配置檔案以定義輸入顏色空間。 如果源影像中沒有嵌入配置檔案， `attribute::IccProfileSrc*` 使用對應於源影像的像素類型的適用影像目錄。 如果未在影像目錄中定義此屬性， `attribute::IccProfile*` 的子菜單。 如果也未定義該目錄屬性，則影像不受顏色管理，只應用天真的轉換。

## 輸出顏色空間 {#section-b517bca622b64dcfa7defba6035d0716}

使用 `icc=` 的子菜單。 如果 `icc=` 未指定，則與輸出影像的像素類型對應的預設輸出顏色空間（來自請求的主目錄）用作輸出顏色空間。 如果在主目錄或預設目錄中未定義輸出配置檔案，並且如果基本層是具有與輸出像素類型匹配的嵌入式配置檔案的影像，則該配置檔案將用於輸出顏色空間。 否則，輸出顏色空間仍未定義 — 在像素類型之間轉換時只應用天真的顏色轉換，並且輸出影像中不能嵌入任何顏色配置檔案。

嵌套/嵌入式影像服務請求的輸出顏色空間始終與外部嵌入請求的輸出顏色空間相同。

## 純色 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

指定的顏色值 `color=`。 `bgcolor=`或RTF命令 `\iscolortbl` 如果顏色值包括尾碼「S」，則與輸入顏色空間關聯，否則，它們與輸出顏色空間關聯。 指定的顏色值 `bgc=` 或RTF命令 `\colortbl` 和 `\cmykcolortbl` 始終與相應的預設或實際輸出顏色空間關聯。

>[!NOTE]
>
>此時， `bgc=` 不完全參與色彩管理 — 當指定時忽略「S」尾碼 `bgc=`，並且當使用指定的顏色值的像素類型時應用天真轉換 `bgc=` 與輸出影像的像素類型不同。 否則， `bgc=` 與實際輸出顏色空間關聯。

## 嵌套和嵌入式請求 {#section-bdda638c31504f26a77e51ebb1ea6e3b}

嵌套IS請求和嵌入IR請求的輸出顏色空間被自動設定為最外請求的輸出顏色空間，除非嵌套請求指定具有 `icc=`。 此外，嵌套/嵌入式請求還從最外層請求的主目錄繼承預設輸出顏色空間，以確保對實色值的一致處理。

## 顏色空間轉換 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

影像服務通常嘗試在處理期間延遲顏色轉換。 如果影像的所有圖層具有相同的圖層顏色空間，則在合併和最終縮放後將完成對輸出顏色空間的轉換。 如果涉及多層顏色空間，則在合併之前將每個層轉換為輸出顏色空間。

>[!NOTE]
>
>命令 `op_brightness=`。 `op_colorbalance=`。 `op_colorize=`。 `op_contrast=`。 `op_hue=`, `op_saturation=` 是RGB。 這些操作僅在圖層顏色空間具有RGB像素類型時才保持顏色保真度。 如果除RGB外，資料使用天真的顏色轉換被轉換為RGB，並且結果的顏色保真度將有限。 此類圖層的圖層顏色空間應視為不確定。

提供顏色轉換選項 `icc=` 或 `icc=` 未指定，使用 `attribute::IccRenderIntent`。 `attribute::IccBlackPointCompensation`, `attribute::IccDither`。

## 嵌入顏色配置檔案 {#section-261ebbae5ce046589a776ca972380052}

輸出顏色空間的ICC顏色配置檔案（如果可用）可通過指定來嵌入到響應影像中 `iccEmbed=`。

## 管理ICC配置檔案 {#section-eb210e4b44e64e2c8b80ee59216c5555}

伺服器使用的所有顏色配置檔案必須符合ICC規範。 ICC配置檔案通常具有 [!DNL .icc] 或 [!DNL .icm] 檔案尾碼，與影像資料檔案共址。

而輸出配置檔案可以通過 `icc=` 命令，建議在預設目錄或影像目錄的ICC配置檔案映射中註冊所有配置檔案並使用快捷方式標識符( `icc::Name`)而不是檔案路徑。

中引用的所有ICC配置檔案 `catalog::IccProfile` 在 `attribute::IccProfile*` 必須在影像或預設目錄的ICC配置檔案映射中註冊。

## 限制 {#section-fb50ede40b124b89b30679da29782ab5}

目前僅支援CMYK、RGB和灰階色彩空間。

## 包括的ICC顏色配置檔案 {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Image Serving在預設映像目錄中包括大多數標準AdobeICC配置檔案。 這些檔案可通過其共同名稱(如Photoshop所見)或稍短的標識符訪問。 下表列出了所有標準ICC配置檔案。 在中引用配置檔案時 `icc=` 命令，空格必須編碼為 `%20`。

可以將附加配置檔案添加到標準配置檔案中，即添加到預設目錄或特定影像目錄中。 請參閱 [ICC配置檔案映射參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) 的雙曲餘切值。

>[!NOTE]
>
>下表適用於 *Dynamic Media* 僅（運行） `dynamicmedia` 運行模式)。

|標識符|公用名|檔案名| |— |— |— | |**RGB**|| |`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc| |`AppleRGB`|AppleRGB|AppleRGB.icc| |`CIERGB`|CIERGB|CIERGB.icc| |`ColorMatchRGB`|ColorMatchRGB|ColorMatchRGB.icc| |`NTSC`|NTSC(1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto`|ProPhotoRGB|ProPhoto.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb色彩空間配置檔案.icm| |`WideGamutRGB`|寬色域RGB|WideGamtRGB.icc| |**CMYK**|| |`CoatedFogra27`|Cobided FOGRA27(ISO 12647-2:2004)|CobidedFOGRA27.icc| |`CoatedFogra39`|Cobided FOGRA39(ISO 12647-2:2004)|CobidedFOGRA39.icc| |`CoatedGraCol`|Cobided GRACoL 2006(ISO 12647-2:2004)|CobidedGRACoL2006.icc| |`EuropeISOCoated`|Europe ISO Cobided FOGRA27|EuropeISOCoatedFOGRA27.icc| |`EuroscaleCoated`|Euroscale Cobded|EuroscaleCobded.icc| |`EuroscaleUncoated`|Euroscale Uncoved v2|EuroscaleUncoved.icc| |`JapanColorCoated`|Japan Color 2001 Cobted|JapanColor2001Cobid.icc| |`JapanColorNewspaper`|Japan Color 2002 Heapper|JapanColor2002Heapper.icc| |`JapanColorUncoated`|Japan Color 2001 Uncovided|JapanColor2001Uncovided.icc| |`JapanColorWebCoated`|Japan Color 2003 Web Cobided|JapanColor2003WebCobid.icc| |`JapanWebCoated`|Japan Web Cobded(Ad)|JapanWebCobd.icc| |`NewsprintSNAP2007`|US新聞紙(SNAP 2007)|USNewsprintSNAP2007.icc| |`PS4Default`|Photoshop4預設CMYK|Photoshop4DefaultCMYK.icc| |`PS5Default`|Photoshop5預設CMYK|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|USSheetfed Cobfid v2|USSheetfedCobfid.icc| |`SheetfedUncoated`|USSheetfed Uncoved v2|USSheetfedUncoved.icc| |`UncoatedFogra29`|Uncobed FOGRA29(ISO 12647-2:2004)|UncobidedFOGRA29.icc| |`WebCoated`|USWeb Cobided(SWOP)v2|USWebCobidedSWOP.icc| |`WebCoatedFogra28`|Web Cobided FOGRA28(ISO 12647-2:2004)|WebCobidedFOGRA28.icc| |`WebCoatedGrade3`|Web Cobided SWOP 2006 3級紙|WebCobidedSWOP2006 3.icc| |`WebCoatedGrade5`|Web Cobided SWOP 2006 Grade 5 Paper|WebCobidedSWOP2006Grade 5.icc| |`WebUncoated`|USWeb Uncoved v2|USWebUncoved.icc|

下表適用於 *Dynamic Media Classic影像服務* 和 *Dynamic Media* (正在運行 `dynamicmedia_scene7` 運行模式)。

|標識符|公用名|檔案名| |— |— |— | |**RGB**|| |`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc| |`AppleRGB`|AppleRGB|AppleRGB.icc| |`CIERGB|CIE RGB`|CIERGB.icc| |`ColorMatchRGB`|ColorMatchRGB|ColorMatchRGB.icc| |`NTSC`|NTSC(1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto RGB`|ProPhotoRGB|ProPhotoRGB.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb色彩空間配置檔案.icm| |`WideGamutRGB`|寬色域RGB|WideGamtRGB.icc| |**CMYK**|| |`CoatedFogra27`|Cobided FOGRA27(ISO 12647-2:2004)|CobidedFOGRA27.icc| |`CoatedFogra39`|Cobided FOGRA39(ISO 12647-2:2004)|CobidedFOGRA39.icc| |`Coated GRACoL 2006 (ISO 12647-2:2004)`|Cobided GRACoL 2006(ISO 12647-2:2004)|CobidedGRACoL2006.icc| |`EuropeISOCoated`|Europe ISO Cobided FOGRA27|EuropeISOCoatedFOGRA27.icc| |`Euroscale Coated v2`|Euroscale Cobded v2|EuroscaleCobped.icc| |`EuroscaleUncoated`|Euroscale Uncoved v2|EuroscaleUncoved.icc| |`JapanColorCoated`|Japan Color 2001 Cobted|JapanColor2001Cobid.icc| |`JapanColorNewspaper`|Japan Color 2002 Heapper|JapanColor2002Heapper.icc| |`JapanColorUncoated`|Japan Color 2001 Uncovided|JapanColor2001Uncovided.icc| |`Japan Color 2003 Web Coated`|Japan Color 2003 Web Cobided|JapanColor2003WebCobid.icc| |`JapanWebCoated`|Japan Web Cobded(Ad)|JapanWebCobd.icc| |`PS4Default`|Photoshop4預設CMYK|Photoshop4DefaultCMYK.icc| |`PS5Default`|Photoshop5預設CMYK|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|USSheetfed Cobfid v2|USSheetfedCobfid.icc| |`SheetfedUncoated`|USSheetfed Uncoved v2|USSheetfedUncoved.icc| |`UncoatedFogra29`|Uncobed FOGRA29(ISO 12647-2:2004)|UncobidedFOGRA29.icc| |`US Newsprint (SNAP 2007)`|US新聞紙(SNAP 2007)|USNewsprintSNAP2007.icc| |`WebCoated`|USWeb Cobided(SWOP)v2|USWebCobidedSWOP.icc| |`WebCoatedFogra28`|Web Cobided FOGRA28(ISO 12647-2:2004)|WebCobidedFOGRA28.icc| |`Web Coated SWOP 2006 Grade 3 Paper`|Web Cobided SWOP 2006 3級紙|WebCobidedSWOP2006 3.icc| |`Web Coated SWOP Grade 5 Paper`|Web Cobided SWOP 2006 Grade 5 Paper|WebCobidedSWOP2006Grade 5.icc| |`WebUncoated`|USWeb Uncoved v2|USWebUncoved.icc|

## 另請參閱 {#section-39159397e80b4efca5f631eab8b9aa06}

[國際顏色聯盟](https://www.color.org/index.xalter)。 [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)。 [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)。 [屬性：:IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*, [屬性：:IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*, [屬性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)。 [屬性：:IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)。 [屬性：:IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)。 [ICC配置檔案映射參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)。 [顏色=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)。 [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)。 [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
