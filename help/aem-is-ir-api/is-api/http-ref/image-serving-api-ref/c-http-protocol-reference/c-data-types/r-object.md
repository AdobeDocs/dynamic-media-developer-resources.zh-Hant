---
description: 源對象說明符。 可以將影像、SVG和ICC配置檔案對象指定為影像目錄條目或相對檔案路徑
solution: Experience Manager
title: 物件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 1%

---

# 物件{#object}

源對象說明符。 可以將影像、SVG和ICC配置檔案對象指定為影像目錄條目或相對檔案路徑

`*``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>影像目錄的名稱（<span class="codeph">屬性：:RootId </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、主目錄或預設影像目錄中的影像、SVG、模板或ICC配置檔案記錄的id </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 路徑  </span> </span> </p> </td> 
  <td class="stentry"> <p>相對影像、掩碼或ICC配置檔案路徑和名稱 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 物件  </span> </span> </p> </td> 
  <td class="stentry"> <p>可能發生在主URL路徑中，或發生在<span class="codeph"> src= </span>、<span class="codeph"> mask= </span>或<span class="codeph"> icc= </span>命令中 </p> </td> 
 </tr> 
</table>

*`rootId`* 標識影像目錄。（如需詳細資訊，請參閱[影像目錄](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)。） 如果在URL路徑中指定&#x200B;*`rootId`*，該目錄將成為此請求的&#x200B;*主目錄*。 否則，預設目錄將用作主目錄。 同一請求中可以使用多個不同的影像目錄。

伺服器最初假定`src=`、`mask=`和`icc=`命令中省略&#x200B;*`rootId`*，並將嘗試在主目錄中查找目錄條目。 伺服器會嘗試將整個&#x200B;*`object`*&#x200B;字串有效地用作&#x200B;*`objId.`*

如果找到目錄項，則使用；否則，伺服器下次嘗試匹配影像目錄的&#x200B;*`rootId`*。 如果標識了目錄，則會搜索&#x200B;*`objId`*。 如果找到和項目，則會使用它。

否則，將&#x200B;*`object`*&#x200B;假定為顯式檔案路徑。 在此情況下，如果在主目錄中設定了`attribute::FullMatch`，則會忽略此物件的目錄，並改用預設目錄。 如果未設定`attribute::FullMatch`，則使用主目錄進行進一步處理。

*`rootId`*&#x200B;和&#x200B;*`objId`*&#x200B;都區分大小寫。 *`path`* 僅在UNIX上區分大小寫。

如果指定前導「/」，則會搜尋預設目錄，而非主目錄。 當明確路徑要求`default::RootPath`而非主目錄的`attribute::RootPath`時，這主要很有用，但也可用於訪問預設目錄中的條目，否則這些條目將被主目錄中的條目覆蓋。

有關如何將&#x200B;*`path`*&#x200B;轉換為物理檔案路徑的詳細資訊，請參閱&#x200B;*伺服器配置指南*&#x200B;中的&#x200B;*管理內容*。

>[!NOTE]
>
>*`object.`*&#x200B;中不允許使用逗號「，」字元

## 支援的影像檔案格式 {#section-12c85aead78e4f759856ca9ff10637d7}

有關支援的檔案格式的完整清單，請參閱IC(Image Converter)實用程式的說明。

使用Dynamic Media金字塔TIFF(PTIF)多解析度格式時，需要多個不同解析度的影像資料的應用程式效能最佳。 IC實用程式用於從任何支援的影像格式建立PTIF影像。

## 範例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**在兩個不同的影像目錄中訪問影像和ICC配置檔案**

在標識為「[!DNL myCatalog]」的映像目錄中檢索映像「[!DNL myImage]」，並附加位於名為「[!DNL myProfiles]」的映像目錄中的ICC配置檔案「[!DNL sRGB]」：

` http:// *`伺服器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

使用具有分層的單個影像目錄

**建立由三層組成的簡單複合影像，所有這些層都從「」中 [!DNL myCatalog]檢索：**

` http:// *`伺服器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**在仍使用目錄提供屬性時直接存取影像檔案**

使用`myImageCatalog`中配置的預設jpg屬性訪問[!DNL my/image/path/myImage.tif]:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另請參閱 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC實用程式](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
