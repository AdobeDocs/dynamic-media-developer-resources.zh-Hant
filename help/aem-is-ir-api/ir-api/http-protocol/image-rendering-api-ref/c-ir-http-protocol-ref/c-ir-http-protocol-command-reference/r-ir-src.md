---
description: 材料檔案。 指定材料資料，以單一材料目錄參考的形式，或以逗號分隔為一或兩個影像或材料資料檔案。
solution: Experience Manager
title: src
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---


# src{#src}

材料檔案。 指定材料資料，以單一材料目錄參考的形式，或以逗號分隔為一或兩個影像或材料資料檔案。

`src = *`catalogEntrymaterialFileembeddedReqmaterialFile`*|{{ *``*| *``*}[, *``*]`

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
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;<span class="varname"> lbrace;'isReq</span>'&amp;rbraces;'ir&amp;rbrace;'ir&amp;lbrace<span class="varname"> '&amp;rbrace;'|&amp;lbrace;'&amp;</span>forienReq<span class="varname"> </span>'&amp;rbraces;'</span> </p></td> 
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
  <td class="stentry"> <p>要求影像伺服。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>要求影像演算。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>向外部伺服器請求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 名稱</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的名稱。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 索引</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的索引號。 </p></td> 
 </tr> 
</table>

可重複的紋理、貼紙和壁紙材料需要單一影像，而此影像可指定為檔案或內嵌請求。

檔案櫃材料需要檔案櫃樣式檔案([!DNL .vnc])，不能將其指定為嵌套請求。 紋理影像檔案對於檔案櫃是可選的，如果指定，則可能是檔案或嵌入請求。

窗口覆蓋材料需要窗口覆蓋樣式檔案([!DNL .vnw])，該檔案不能指定為嵌套請求。 紋理檔案是選用的，如果指定，則可能是檔案或內嵌請求。

「影像演算」使用與「影像伺服」相同的規則來尋找材質型錄、目錄項目和資料檔案。 如需詳細資訊，請參閱影像服務檔案中的&#x200B;*`object`*&#x200B;資料類型說明。

*`materialFile`* 是相對於的路徑 `attribute::RootPath`。

*`foreignReq`* 可以是相對於的URL, `attribute::RootUrl`或絕對URL(若已 `attribute::AllowDirectUrls` 設定)。

如果未指定&#x200B;*`catId`*，則使用會話目錄。

`srcE=` 並提 `srcN=` 供對暗角內嵌材料的存取。

## 支援的檔案格式{#section-f2186d3eef834fc8bbecb2bc68daacad}

「影像演算」支援與「Dynamic Media影像伺服」相同的來源影像格式。

使用Scene7金字塔TIFF(PTIFF)多解析度格式時，需要多種不同解析度的影像資料的應用程式效能最好。 「影像伺服」包含影像轉換器(IC)公用程式，可從任何支援的格式建立PTIFF影像。

有關支援的檔案格式的完整清單，請參閱映像服務文檔中的IC實用程式說明。

## 屬性 {#section-e68d03788d534e2184147987d51dfd0f}

材料屬性。 除純色外的所有材料都需要（不允許純色材料）。 所有字串都區分大小寫。 *`index`* 必須為0或更大。

## 預設 {#section-dde549c1917540dc8f9555962202da3c}

無。

## 範例 {#section-675865444f8a4d35b9fc6e58b36e3438}

具有單獨可重複紋理的彩色機櫃的MSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

同一材料可以位於記錄「 `12-3-2`」中的`'cat`材料目錄中：

`…&obj=cabinets&src=cat/12-3-2&…`

巢狀請求「影像伺服」以取得紋理影像：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 另請參閱 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Material Catalogs](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)，屬 [性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)，屬 [性：:AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
