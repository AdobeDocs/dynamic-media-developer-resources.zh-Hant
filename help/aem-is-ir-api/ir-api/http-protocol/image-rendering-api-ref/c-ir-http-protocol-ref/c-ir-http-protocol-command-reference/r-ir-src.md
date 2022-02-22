---
title: 高
description: 材料檔案。 指定材料資料（以單個材料目錄引用的形式），或以一個或兩個影像或材料資料檔案（用逗號分隔）的形式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 2%

---

# 高{#src}

材料檔案。 指定材料資料（以單個材料目錄引用的形式），或以一個或兩個影像或材料資料檔案（用逗號分隔）的形式。

`src = *`目錄條目`*|{{ *`材料檔案`*| *`嵌入式請求`*}[, *`材料檔案`*]`

`srcE= *`名稱`*`

`srcN= *`索引`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 目錄條目</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> 貓ID</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> 材料檔案</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 樣式檔案</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 嵌入式請求</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace；是&amp;lbrace;'<span class="varname"> 為請求</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rbrace;'|&amp;lbrace;'&amp;lbrace;''<span class="varname"> 外協</span>'&amp;rbrase;</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 貓ID</span> </p></td> 
  <td class="stentry"> <p>物料目錄ID(<span class="codeph"> 屬性：:RootId</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>物料目錄條目(<span class="codeph"> 目錄：:ID</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 樣式檔案</span> </p></td> 
  <td class="stentry"> <p>材料樣式檔案(<span class="filepath"> .vnc</span> 或 <span class="filepath"> .vnw</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>影像資料檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 為請求</span> </p></td> 
  <td class="stentry"> <p>請求影像服務。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>請求影像呈現。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 外協</span> </p></td> 
  <td class="stentry"> <p>請求到外部伺服器。 </p></td> 
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

可重複的紋理、貼花和牆紙材料需要單個影像，該影像可以指定為檔案或嵌入請求。

檔案櫃材料需要檔案櫃樣式檔案( [!DNL .vnc])，不能指定為嵌套請求。 紋理影像檔案對於檔案櫃是可選的，如果指定，則可能是檔案或嵌入請求。

窗口覆蓋材料需要窗口覆蓋樣式檔案( [!DNL .vnw])，不能指定為嵌套請求。 紋理檔案是可選的，如果指定，它可能是檔案或嵌入式請求。

「影像呈現」使用與「影像服務」相同的規則來查找材料目錄、目錄條目和資料檔案。 請參閱 *`object`* 有關詳細資訊，請參閱Image Serving文檔中的資料類型。

*`materialFile`* 是相對於 `attribute::RootPath`。

*`foreignReq`* 可以是相對於 `attribute::RootUrl`或絕對URL `attribute::AllowDirectUrls` 的子菜單。

如果 *`catId`* 未指定，則使用會話目錄。

`srcE=` 和 `srcN=` 提供對嵌在導管中的材料的訪問。

## 支援的檔案格式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

影像呈現支援與Dynamic Media影像服務相同的源影像格式。

使用Scene7金字塔TIFF(PTIFF)多解析度格式時，需要具有多種不同解析度的影像資料的應用程式效能最佳。 影像服務包括影像轉換器(IC)實用程式，該實用程式根據任何支援的格式建立PTIFF影像。

有關支援的檔案格式的完整清單，請參閱映像服務文檔中IC實用程式的說明。

## 屬性 {#section-e68d03788d534e2184147987d51dfd0f}

物料屬性。 除純色外的所有材料都必需（不允許使用純色材料）。 所有字串都區分大小寫。 *`index`* 必須為0或更大。

## 預設 {#section-dde549c1917540dc8f9555962202da3c}

無。

## 範例 {#section-675865444f8a4d35b9fc6e58b36e3438}

用於具有獨立可重複紋理的彩色機櫃的MSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

相同的材料可以在物料目錄中 `'cat`記錄&#39; `12-3-2`「：

`…&obj=cabinets&src=cat/12-3-2&…`

對影像服務的嵌套請求，以獲取紋理影像：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 另請參閱 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[物料目錄](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)。 [屬性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)。 [屬性：:AllowDirectUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
