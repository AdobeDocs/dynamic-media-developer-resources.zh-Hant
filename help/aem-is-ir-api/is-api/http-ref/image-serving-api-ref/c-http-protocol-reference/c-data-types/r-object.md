---
description: 源對象指定符。 影像、SVG和ICC配置檔案對象可以指定為影像目錄條目或相對檔案路徑
solution: Experience Manager
title: 物件
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 1%

---


# object{#object}

源對象指定符。 影像、SVG和ICC配置檔案對象可以指定為影像目錄條目或相對檔案路徑

`*``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>影像目錄的名稱（<span class="codeph">屬性：:RootId </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、主目錄或預設影像目錄中的影像、SVG、範本或ICC描述檔記錄ID </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 路徑  </span> </span> </p> </td> 
  <td class="stentry"> <p>相對影像、蒙版或ICC配置檔案路徑和名稱 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 物件  </span> </span> </p> </td> 
  <td class="stentry"> <p>可能發生在主URL路徑中，或發生在<span class="codeph"> src= </span>、<span class="codeph"> mask= </span>或<span class="codeph"> icc= </span>命令中 </p> </td> 
 </tr> 
</table>

*`rootId`* 標識影像目錄。（如需詳細資訊，請參閱[影像目錄](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)。） 如果在URL路徑中指定&#x200B;*`rootId`*，該目錄將成為此請求的&#x200B;*主目錄*。 否則，將使用預設目錄作為主目錄。 同一個請求中可使用多個不同的影像目錄。

伺服器最初假定`src=`、`mask=`和`icc=`命令中省略&#x200B;*`rootId`*，並將嘗試在主目錄中查找目錄條目。 有效地，伺服器會嘗試將整個&#x200B;*`object`*&#x200B;字串用作&#x200B;*`objId.`*

如果找到目錄條目，則使用；否則，伺服器下次嘗試匹配映像目錄的&#x200B;*`rootId`*。 如果已識別目錄，則會搜尋&#x200B;*`objId`*。 如果找到和條目，則使用它。

否則，假定&#x200B;*`object`*&#x200B;為顯式檔案路徑。 在這種情況下，如果在主目錄中設定了`attribute::FullMatch`，則會忽略此對象的目錄，並改用預設目錄。 如果未設定`attribute::FullMatch`，則使用主目錄進行進一步處理。

*`rootId`*&#x200B;和&#x200B;*`objId`*&#x200B;都區分大小寫。 *`path`* 僅在UNIX上區分大小寫。

如果指定前導&#39;/&#39;，則會搜尋預設目錄，而非主目錄。 當明確路徑需要`default::RootPath`而非主目錄的`attribute::RootPath`時，此功能非常有用，但也可用於訪問預設目錄中的條目，否則這些條目將被主目錄中的條目覆蓋。

有關如何將&#x200B;*`path`*&#x200B;轉換為物理檔案路徑的詳細資訊，請參閱&#x200B;*伺服器配置指南*&#x200B;中的&#x200B;*管理內容*。

>[!NOTE]
>
>*`object.`*&#x200B;中不允許逗號&#39;,&#39;字元

## 支援的影像檔案格式{#section-12c85aead78e4f759856ca9ff10637d7}

有關支援的檔案格式的完整清單，請參閱IC（影像轉換器）實用程式的說明。

使用Dynamic Media金字塔TIFF(PTIF)多解析度格式時，需要多種不同解析度的影像資料的應用程式效能最好。 IC實用程式用於從任何支援的影像格式建立PTIF影像。

## 範例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**在兩個不同的影像目錄中存取影像和ICC描述檔**

在標識為「 [!DNL myCatalog]」的映像目錄中檢索映像「 [!DNL myImage]」，並附加位於名為「 [!DNL myProfiles]」的映像目錄中的ICC配置檔案「 [!DNL sRGB]」:

` http:// *`伺服器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

使用單一影像目錄及分層

**建立由三個圖層組成的簡單複合影像，全部都是從「 [!DNL myCatalog]」擷取：**

` http:// *`伺服器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**直接存取影像檔案，同時仍使用目錄提供屬性**

使用`myImageCatalog`中設定的預設jpg屬性，存取[!DNL my/image/path/myImage.tif]:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另請參閱 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC實用程式](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
