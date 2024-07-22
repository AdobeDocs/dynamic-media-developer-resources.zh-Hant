---
title: 影像伺服色彩管理
description: 「影像伺服」支援根據符合ICC （國際色彩聯盟）規格的色域設定檔進行色域轉換。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1220'
ht-degree: 0%

---

# 影像伺服色彩管理{#image-serving-color-management}

「影像伺服」支援根據符合ICC （國際色彩聯盟）規格的色域設定檔進行色域轉換。

## 預設色彩空間 {#section-8cfe60808bce49968091995e4e521dba}

每個影像目錄（和預設目錄）可以定義一組ICC設定檔，這些設定檔構成此目錄的預設色彩空間 — 灰階、RGB和CMYK資料各有一個輸入和一個輸出設定檔。 另請參閱
[attribute：：IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute：：IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute：：IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute：：IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute：：IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute：：IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md)。

## 輸入色域 {#section-9f08e2c1b6aa4fe4815be174972c1944}

Source影像可內嵌ICC設定檔以定義輸入色域。 如果來源影像中沒有內嵌設定檔，則會使用與來源影像的畫素型別對應的適用影像目錄`attribute::IccProfileSrc*`。 如果未在影像目錄中定義此屬性，則會使用`attribute::IccProfile*`。 如果未定義該目錄屬性，則影像不會以色彩管理，只會套用天真的轉換。

## 輸出色域 {#section-b517bca622b64dcfa7defba6035d0716}

要求之最終影像結果的色域是以`icc=`命令定義。 如果未指定`icc=`，則會使用與輸出影像的畫素型別對應的預設輸出色域（來自請求的主要目錄）作為輸出色域。 如果主要目錄或預設目錄中未定義輸出設定檔，且基本圖層是具有符合輸出畫素型別的內嵌設定檔的影像，則該設定檔會用於輸出色域。 否則，輸出色域會維持未定義 — 在畫素型別之間進行轉換時，只會套用單純的色彩轉換，而且輸出影像中不會嵌入任何色彩設定檔。

巢狀/內嵌「影像伺服」請求的輸出色域一律與嵌入請求外部的輸出色域相同。

## 純色 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

如果色彩值包含尾碼&#39;S&#39;，則以`color=`、`bgcolor=`或RTF命令`\iscolortbl`指定的色彩值會與輸入色域相關聯，否則會與輸出色域相關聯。 以`bgc=`或RTF命令`\colortbl`和`\cmykcolortbl`指定的色彩值永遠與對應的預設或實際輸出色彩空間相關聯。

>[!NOTE]
>
>此時，`bgc=`未完全參與色彩管理 — 使用`bgc=`指定時，會忽略&#39;S&#39;尾碼，而且當使用`bgc=`指定的色彩值的畫素型別與輸出影像的畫素型別不同時，會套用天真的轉換。 否則，`bgc=`會與實際輸出色域相關聯。

## 巢狀內嵌請求 {#section-bdda638c31504f26a77e51ebb1ea6e3b}

巢狀IS要求與內嵌IR要求的輸出色域會自動設定為最外層要求的輸出色域，除非巢狀要求指定明確的輸出色域為`icc=`。 此外，巢狀/內嵌請求也會繼承最外層請求之主目錄的預設輸出色域，以確保處理純色值的一致性。

## 色域轉換 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

「影像伺服」通常會在處理期間嘗試延遲色彩轉換。 如果影像的所有圖層都具有相同的圖層色域，則會在合併和最終縮放後轉換為輸出色域。 如果涉及多個圖層色域，每個圖層都會先轉換成輸出色域，然後再合併。

>[!NOTE]
>
>命令`op_brightness=`、`op_colorbalance=`、`op_colorize=`、`op_contrast=`、`op_hue=`和`op_saturation=`是RGB作業。 只有在圖層色域具有RGB畫素型別時，這些作業才會維持色彩逼真度。 如果除了RGB之外，資料會使用原始色彩轉換轉換為RGB，而結果會具有有限的色彩逼真度。 這些圖層的圖層色域應視為不確定。

色彩轉換選項是與`icc=`一起提供，如果未指定`icc=`，則與`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`和`attribute::IccDither`一起提供。

## 嵌入色彩設定檔 {#section-261ebbae5ce046589a776ca972380052}

輸出色域的ICC色彩設定檔（如果可用）可透過指定`iccEmbed=`嵌入回應影像。

## 管理ICC設定檔 {#section-eb210e4b44e64e2c8b80ee59216c5555}

伺服器使用的所有色彩設定檔都必須符合ICC規格。 ICC設定檔通常有[!DNL .icc]或[!DNL .icm]檔案字尾，而且與影像資料檔位於同一位置。

雖然輸出設定檔可以由`icc=`命令中的檔案路徑/名稱指定，但建議在預設目錄或影像目錄的ICC設定檔對應中註冊所有設定檔，並使用捷徑識別碼( `icc::Name`)而不是檔案路徑。

在`catalog::IccProfile`和`attribute::IccProfile*`中參考的所有ICC設定檔都必須在影像或預設目錄的ICC設定檔對應中註冊。

## 限制 {#section-fb50ede40b124b89b30679da29782ab5}

目前僅支援CMYK、RGB和灰階色域。

## 包含的ICC色彩設定檔 {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

「影像伺服」包含預設影像目錄中的大部分標準AdobeICC設定檔。 這些設定檔可透過其通用名稱(例如，如Photoshop中所見)或較短的識別碼來存取。 下表列出所有標準ICC設定檔。 以設定檔的通用名稱參照`icc=`命令中的設定檔時，必須將空格編碼為`%20`。

可以將其他設定檔新增至標準設定檔，即預設目錄或特定影像目錄。 如需詳細資訊，請參閱[ICC設定檔對應參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)。

>[!NOTE]
>
>下表僅適用於&#x200B;*Dynamic Media混合式* （在`dynamicmedia`執行模式下執行）。

| 識別碼 | 一般名稱 | 檔案名稱 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | AppleRGB | AppleRGB.icc |
| `CIERGB` | CIERGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatchRGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | pal_SECAM.icc |
| `ProPhoto` | ProPhotoRGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb色域Profile.icm |
| `WideGamutRGB` | 寬色域RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | 歐洲ISO銅版FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001塗裝 | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002報紙 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated （廣告） | JapanWebCoated.icc |
| `NewsprintSNAP2007` | 美國新聞紙(SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4預設CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5預設CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | 無塗層的FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Web Coated SWOP 2006 Grade 3紙 | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Web Coated SWOP 2006 Grade 5紙張 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

下表適用於&#x200B;*Dynamic Media Classic影像伺服*&#x200B;和&#x200B;*Dynamic Media* （在`dynamicmedia_scene7`執行模式中執行）。

| 識別碼 | 一般名稱 | 檔案名稱 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | AppleRGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatchRGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | pal_SECAM.icc |
| `ProPhoto RGB` | ProPhotoRGB | ProPhotoRGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb色域Profile.icm |
| `WideGamutRGB` | 寬色域RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | 歐洲ISO銅版FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001塗裝 | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002報紙 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated （廣告） | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4預設CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5預設CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | 無塗層的FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | 美國新聞紙(SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Web Coated SWOP 2006 Grade 3紙 | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Web Coated SWOP 2006 Grade 5紙張 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## 另請參閱 {#section-39159397e80b4efca5f631eab8b9aa06}

[國際色彩協會](https://www.color.org/index.xalter)，[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)，[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)，[attribute：：IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;，[attribute：：IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;，[attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，[attribute：：IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)，[attribute：：IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)，[ICC設定檔對應圖參考7}，[COLOR=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)，[BGC=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)，[*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)
