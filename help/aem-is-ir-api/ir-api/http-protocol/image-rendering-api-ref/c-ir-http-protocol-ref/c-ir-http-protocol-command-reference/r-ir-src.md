---
description: 材料檔案。 指定材料資料，以單個材料目錄引用的形式，或以一個或兩個影像或材料資料檔案的形式，以逗號分隔。
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# src{#src}

材料檔案。 指定材料資料，以單個材料目錄引用的形式，或以一個或兩個影像或材料資料檔案的形式，以逗號分隔。

`src = *``*|{{ *``*| *``*}[, *`catalogEntrymaterialFileembeddedReqmaterialFile`*]`

`srcE= *`名稱`*`

`srcN= *`索引`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rbrace;'|&amp;lbrace;'&amp;lbrace;'&amp;lbrace;'<span class="varname"> forigReq</span>'&amp;rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>材料目錄ID（<span class="codeph">屬性：:RootId</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>物料目錄條目（<span class="codeph">目錄：:Id</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>材料樣式檔案（<span class="filepath"> .vnc</span>或<span class="filepath"> .vnw</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>影像資料檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>請求影像伺服。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>影像呈現請求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>向外部伺服器發出請求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 名稱</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的名稱。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 索引</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的索引號為0。 </p></td> 
 </tr> 
</table>

可重複的紋理、貼牌和壁紙材料需要單個影像，可以指定為檔案或嵌入請求。

檔案櫃材料需要檔案櫃樣式檔案([!DNL .vnc])，不能將其指定為嵌套請求。 紋理影像檔案對於檔案櫃是可選的，如果指定，它可以是檔案或嵌入請求。

窗口覆蓋材料需要窗口覆蓋樣式檔案([!DNL .vnw])，不能將其指定為嵌套請求。 紋理檔案是可選的，如果指定，它可以是檔案或嵌入請求。

「影像呈現」使用與「影像伺服」相同的規則來尋找材料目錄、目錄項目和資料檔案。 如需詳細資訊，請參閱影像伺服檔案中&#x200B;*`object`*&#x200B;資料類型的說明。

*`materialFile`* 是相對於的路 `attribute::RootPath`徑。

*`foreignReq`* 可以是相對於的URL, `attribute::RootUrl`或是絕對URL(若 `attribute::AllowDirectUrls` 已設定)。

如果未指定&#x200B;*`catId`*，則使用會話目錄。

`srcE=` 提供 `srcN=` 對嵌入在暈船中的材料的訪問。

## 支援的檔案格式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

「影像轉譯」支援與Dynamic Media Image Serving相同的來源影像格式。

使用Scene7金字塔TIFF(PTIFF)多解析度格式時，需要多個不同解析度的影像資料的應用程式效能最佳。 「影像服務」包括「影像轉換器(IC)」實用程式，該實用程式從任何受支援的格式建立PTIFF影像。

如需完整的支援檔案格式清單，請參閱影像伺服檔案中IC公用程式的說明。

## 屬性 {#section-e68d03788d534e2184147987d51dfd0f}

材料屬性。 除實色外的所有材料都需要（實色材料不允許）。 所有字串均區分大小寫。 *`index`* 必須為0或更大。

## 預設 {#section-dde549c1917540dc8f9555962202da3c}

無。

## 範例 {#section-675865444f8a4d35b9fc6e58b36e3438}

具有獨立可重複紋理的彩色機櫃的MSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

同一材料可以位於記錄「`12-3-2`」中的材料目錄`'cat`中：

`…&obj=cabinets&src=cat/12-3-2&…`

對「影像伺服」的巢狀請求，以獲得紋理影像：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 另請參閱 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[材料目錄](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [屬性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [屬性：:AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
