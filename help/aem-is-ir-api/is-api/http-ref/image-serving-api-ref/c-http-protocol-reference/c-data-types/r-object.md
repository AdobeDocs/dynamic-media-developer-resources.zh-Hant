---
description: 源對象說明符。 影像、SVG和ICC配置檔案對象可以指定為影像目錄條目或相對檔案路徑
solution: Experience Manager
title: 物件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# 物件{#object}

源對象說明符。 影像、SVG和ICC配置檔案對象可以指定為影像目錄條目或相對檔案路徑

`*`對象`*[/]{[ *`根ID`*/] *`objId`*}| *`路徑`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 根ID </span> </span> </p> </td> 
  <td class="stentry"> <p>映像目錄的名稱( <span class="codeph"> 屬性：:RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、主目錄或預設映像目錄中的映像、SVG、模板或ICC配置檔案記錄的id </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 路徑 </span> </span> </p> </td> 
  <td class="stentry"> <p>相對影像、蒙版或ICC配置檔案路徑和名稱 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 對象 </span> </span> </p> </td> 
  <td class="stentry"> <p>可能發生在主URL路徑中，或 <span class="codeph"> src= </span>。 <span class="codeph"> 掩碼= </span>或 <span class="codeph"> icc= </span> 命令 </p> </td> 
 </tr> 
</table>

*`rootId`* 標識影像目錄。 (請參閱 [影像目錄](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 。) 如果 *`rootId`* 在URL路徑中指定，該目錄將成為 *主目錄* 請求。 否則，將預設目錄用作主目錄。 在同一請求中可以使用多個不同的影像目錄。

伺服器最初假定 *`rootId`* 在中省略 `src=`。 `mask=`, `icc=` 命令，並嘗試在主目錄中查找目錄條目。 有效地，伺服器嘗試使用 *`object`* 字串 *`objId.`*

如果找到目錄條目，則使用；否則，伺服器將嘗試 *`rootId`* 影像目錄。 如果標識了目錄，則搜索該目錄 *`objId`*。 如果找到並輸入，則使用它。

否則， *`object`* 假定為顯式檔案路徑。 在這種情況下，如果 `attribute::FullMatch` 在主目錄中設定，則忽略此對象的目錄，而改用預設目錄。 如果 `attribute::FullMatch` 未設定，則使用主目錄進行進一步處理。

兩者 *`rootId`* 和 *`objId`* 區分大小寫。 *`path`* 僅在UNIX上區分大小寫。

如果前導 `/` 指定時，將搜索預設目錄而不是主目錄。 當顯式路徑要求 `default::RootPath` 而不是主目錄 `attribute::RootPath`，但也可以用於訪問預設目錄中的條目，否則這些條目將被主目錄中的條目覆蓋。

請參閱 *管理內容* 的 *伺服器配置指南* 有關 *`path`* 轉換為物理檔案路徑。

>[!NOTE]
>
>中不允許使用逗號「，」字元 *`object.`*

## 支援的影像檔案格式 {#section-12c85aead78e4f759856ca9ff10637d7}

有關支援的檔案格式的完整清單，請參閱IC（影像轉換器）實用程式的說明。

當使用Dynamic Media金字塔TIFF(PTIF)多解析度格式時，需要以多種不同解析度的影像資料的應用效果最好。 IC實用程式用於根據任何支援的影像格式建立PTIF影像。

## 範例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**在兩個不同的映像目錄中訪問映像和ICC配置檔案**

檢索映像「 [!DNL myImage]「 」在標識為「 [!DNL myCatalog]&#39;並附加ICC配置檔案&#39; [!DNL sRGB]「 」位於名為「 」的映像目錄中 [!DNL myProfiles]「：

` http:// *`伺服器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

使用具有分層的單個影像目錄

**構建由三個層組成的簡單複合影像，所有層都從「 」檢索 [!DNL myCatalog]「：**

` http:// *`伺服器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**直接訪問影像檔案，同時仍使用目錄提供屬性**

訪問 [!DNL my/image/path/myImage.tif]，使用中配置的預設jpg屬性 `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另請參閱 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC實用程式](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)。 [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)。 [掩碼=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)。 [屬性：:FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
