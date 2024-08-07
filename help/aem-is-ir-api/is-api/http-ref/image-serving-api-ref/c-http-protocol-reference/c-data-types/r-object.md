---
description: Source物件規範。 可以將影像、SVG和ICC設定檔物件指定為影像目錄專案或相對檔案路徑
solution: Experience Manager
title: 物件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# 物件{#object}

Source物件規範。 可以將影像、SVG和ICC設定檔物件指定為影像目錄專案或相對檔案路徑

`*`物件`*[/]{[ *`rootId`*/] *`objId`*}| *`路徑`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>影像目錄的名稱（ <span class="codeph">屬性：：RootId </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">物件ID </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、主要或預設影像目錄中的影像、SVG、範本或ICC設定檔記錄的id </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">路徑</span> </span> </p> </td> 
  <td class="stentry"> <p>相對影像、遮色片或ICC設定檔檔案路徑與名稱 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">物件</span> </span> </p> </td> 
  <td class="stentry"> <p>可能在主要URL路徑中或<span class="codeph"> src= </span>、<span class="codeph"> mask= </span>或<span class="codeph"> icc= </span>命令中發生 </p> </td> 
 </tr> 
</table>

*`rootId`*&#x200B;識別影像目錄。 （如需詳細資訊，請參閱[影像目錄](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)。） 如果在URL路徑中指定&#x200B;*`rootId`*，該目錄會變成此請求的&#x200B;*主目錄*。 否則，會使用預設目錄作為主目錄。 同一個請求中可以使用多個不同的影像目錄。

伺服器最初假設`src=`、`mask=`和`icc=`命令中省略&#x200B;*`rootId`*，並嘗試在主目錄中尋找目錄專案。 實際上，伺服器會嘗試使用整個&#x200B;*`object`*&#x200B;字串做為&#x200B;*`objId.`*

如果找到目錄專案，則會使用它；否則，伺服器接下來會嘗試比對影像目錄的&#x200B;*`rootId`*。 如果識別了目錄，則會搜尋&#x200B;*`objId`*。 如果找到和專案，則會使用它。

否則，會將&#x200B;*`object`*&#x200B;假定為明確的檔案路徑。 在此案例中，如果在主目錄中設定`attribute::FullMatch`，則會忽略此物件的目錄，並改用預設目錄。 如果未設定`attribute::FullMatch`，則會使用主目錄進行進一步處理。

*`rootId`*&#x200B;和&#x200B;*`objId`*&#x200B;都區分大小寫。 *`path`*&#x200B;僅在UNIX上區分大小寫。

如果指定前導字元`/`，則會搜尋預設目錄，而非主要目錄。 當明確路徑需要`default::RootPath`而不是主要目錄的`attribute::RootPath`時，這主要是很有用的，但也可用於存取預設目錄中的專案，否則這些專案會被主要目錄中的專案覆寫。

請參閱&#x200B;*伺服器設定指南*&#x200B;中的&#x200B;*管理內容*，以取得有關如何將&#x200B;*`path`*&#x200B;轉譯為實體檔案路徑的詳細資訊。

>[!NOTE]
>
>*`object.`*&#x200B;中不允許逗號&#39;，&#39;字元

## 支援的影像檔案格式 {#section-12c85aead78e4f759856ca9ff10637d7}

如需支援檔案格式的完整清單，請參閱IC （影像轉換程式）公用程式的說明。

需要多個不同解析度影像資料的應用程式，在使用Dynamic Media金字塔TIFF(PTIF)多解析度格式時表現最佳。 IC公用程式可用來從任何支援的影像格式建立PTIF影像。

## 範例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**存取兩個不同影像目錄中的影像和ICC設定檔**

擷取識別為&#39;[!DNL myCatalog]&#39;之影像目錄中的影像&#39;[!DNL myImage]&#39;，並附加位於名為&#39;[!DNL myProfiles]&#39;之影像目錄中的ICC設定檔&#39; [!DNL sRGB]&#39;：

` http:// *`伺服器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

使用具有分層的單一影像目錄

**建置包含三個圖層的簡單複合影像，全部擷取自&#39;[!DNL myCatalog]&#39;：**

` http:// *`伺服器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**直接存取影像檔案，同時仍使用目錄來提供屬性**

使用`myImageCatalog`中設定的預設jpg屬性存取[!DNL my/image/path/myImage.tif]：

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另請參閱 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC公用程式](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)，[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)，[遮罩=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)，[屬性：：FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
