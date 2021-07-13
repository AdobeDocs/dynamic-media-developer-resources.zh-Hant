---
description: 請求類型. 指定請求的資料類型。
solution: Experience Manager
title: 請求
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 4%

---

# 請求{#req}

請求類型. 指定請求的資料類型。

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 偵錯  </span> </p> </td> 
  <td class="stentry"> <p>在調試模式下運行命令。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 內容 </span> </p> </td> 
  <td class="stentry"> <p>傳回暈映中物件的相關資訊。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>運行命令並返回呈現的影像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops  </span> </p> </td> 
  <td class="stentry"> <p>傳回指定暈映的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 地圖 </span> </p> </td> 
  <td class="stentry"> <p>傳回內嵌於暈映中的影像地圖資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> object </span> </p> </td> 
  <td class="stentry"> <p>運行命令，並將渲染的影像遮罩到當前對象選擇中。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>運行命令並返回回復影像的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata  </span> </p> </td> 
  <td class="stentry"> <p>傳回<span class="codeph">暈映：:UserData </span>的內容。 </p> </td> 
 </tr> 
</table>

除非詳細說明中另有說明，否則伺服器會傳回MIME類型為&lt;text/plain>的文字回應。

`debug`

執行指定的命令並返回呈現的影像。 如果發生錯誤，則返回錯誤和調試資訊，而不是錯誤影像(`attribute::ErrorImagePath`)。

`contents`

傳回暈映中物件階層的XML表示法，包括選取的物件屬性。 請求中的其他命令會被忽略。

`img`

執行指定的命令並返回呈現的影像。 回復資料格式和回應類型由`fmt=`決定。

`imageprops`

返回在URL路徑中指定的暈映檔案或目錄條目的選定屬性。 如需回覆語法和回應MIME類型的說明，請參閱[屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)。 請求中的其他命令會被忽略。 會傳回下列屬性：

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration  </span> </p> </td> 
   <td colname="col2"> <p>雙倍 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：過期 </span> 或預設存留時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td colname="col2"> <p>整數 </p> </td> 
   <td colname="col3"> <p>全解析度高度（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p>與此暈映關聯的配置檔案的名稱/說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile  </span> </p> </td> 
   <td colname="col2"> <p>布林 </p> </td> 
   <td colname="col3"> <p>1如果相關聯的設定檔內嵌於暈映中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths  </span> </p> </td> 
   <td colname="col2"> <p>布林 </p> </td> 
   <td colname="col3"> <p>1如果暈映內嵌路徑資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier  </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：修 </span> 飾詞或空（如果不是目錄條目）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp  </span> </p> </td> 
   <td colname="col2"> <p>列舉 </p> </td> 
   <td colname="col3"> <p>響應影像的像素類型；可以是「CMYK」、「RGB」或「BW」（對於灰度影像）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td colname="col2"> <p>真 </p> </td> 
   <td colname="col3"> <p>預設打印解析度(dpi)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp  </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p>修改日期/時間（來自<span class="codeph">目錄：:TimeStamp </span>或暈映檔案）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td colname="col2"> <p>整數 </p> </td> 
   <td colname="col3"> <p>全解析度寬度（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name  </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p>暈映名稱（根暈映對象的名稱字串）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res  </span> </p> </td> 
   <td colname="col2"> <p>真 </p> </td> 
   <td colname="col3"> <p>以<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">材料解析度</a>單位（通常為像素/英吋）表示的最大對象解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg  </span> </p> </td> 
   <td colname="col2"> <p>真 </p> </td> 
   <td colname="col3"> <p>以<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">材料解析度</a>單位（通常為像素/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">材料解析度</a>h）表示的平均對象解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min  </span> </p> </td> 
   <td colname="col2"> <p>真 </p> </td> 
   <td colname="col3"> <p>最小物件解析度(<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">材料解析度</a>單位（通常為像素/英吋）)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version  </span> </p> </td> 
   <td colname="col2"> <p>整數 </p> </td> 
   <td colname="col3"> <p>暈映檔案版本號。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

傳回暈映中包含的影像地圖資料。 依預設，會傳回所有最外層群組的對應資料。 所有最內層群的地圖資料可以透過

`req=map&groupLevel=-1`

地圖資料不會縮放至`wid=`或`hei=`，或以其他方式修改。 回應MIME類型為`<text/xml>`。

回應資料包含`<map>`元素，其中包含一組`<area>`元素，類似於HTML `<AREA>`標籤。

每個`<area>`元素都包含標準`type=`和`coord=`屬性，以及`name=`屬性，用於指定暈映組名稱或名稱路徑。 如果對應對象組的掩碼具有不連續區域，則存在多個具有相同名稱的`<area>`元素。

除了預設屬性外，如果創作了暈映，還可以定義其他屬性。 此類自訂屬性定義為物件群組屬性。 自訂屬性的名稱必須以`map`開頭。 包含在`<area>`元素中。 例如，如果群組屬性包含`map.href=http://www.scene7.com`，則對應的`<area>`元素將包含`href="http://www.scene7.com"`。

如果暈映不包含映射資料，則返回帶有空`<map>`元素的XML文檔。

`object`

執行指定命令並返回被剩餘對象選擇（請求中最後`sel=`或`obj=`命令選擇的組或對象）遮罩的呈現影像。 通常與支援alpha的影像格式一起使用（請參見[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)）。 如果使用的影像格式不支援Alpha，則遮罩外的區域為黑色。

`props`

執行指定的命令並返回暈映屬性和組或對象屬性，而不是呈現的影像。 有關回覆語法和回應MIME類型的說明，請參閱[屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)。 除非也指定`obj=`或`sel=`（請參閱[ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)），否則預設選擇適用。

回應中可能包含下列屬性：

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>屬性 </p> </th> 
   <th class="entry"> <p> 類型 </p> </th> 
   <th class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回覆影像背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p>整數 </p> </td> 
   <td> <p> 回覆影像高度（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> 布林 </p> </td> 
   <td> <p>如果ICC配置檔案將嵌入回復影像中，則為true（請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與回覆影像相關聯的設定檔的捷徑名稱（請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> 布林 </p> </td> 
   <td> <p> 如果回覆影像包含alpha，則為true。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> 布林 </p> </td> 
   <td> <p> 如果回覆影像包含路徑資料，則為true（請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回復影像類型，可以是「CMYK」、「RGB」或「BW」（對於灰度影像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> 真 </p> </td> 
   <td> <p> 打印解析度(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p>整數，布林值 </p> </td> 
   <td> <p> JPEG品質和色度標幟（請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回覆影像的MIME類型（請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 回覆影像寬度（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 當前選項的屬性字串。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前選項中的對象數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前選項的縮進值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select  <span class="codeph"> selection.attributes  </span>ion.name  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 當前對象選項的全名路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overbling  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前選項中的重疊對象數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p>當前選項中可呈現的對象數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前選項中的可文本化對象數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前選擇的顯示/隱藏狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前選項中第一個重疊對象的Z階值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

返回`vignette::UserData`的內容。 伺服器將用行終結器(`<cr><lf>`)替換`vignette::UserData`中`'??'`的所有出現次數。 回覆的格式為文字資料，回應MIME類型設為&lt;text/plain>。

如果URL路徑中指定的對象未解析為有效的暈映映射條目，或者`vignette::UserData`為空，則答復將僅包含行終結符(`CR/LF`)。

要求字串中的任何其他命令都會遭到忽略。

## 屬性 {#section-e44092e190ff4f6380583e8ed6ea5b0b}

請求命令。 可能發生在要求字串中的任何位置。

## 預設 {#section-00c593cbf1af4364b6b78812e6b93c64}

如果URL不包含影像路徑或修飾元，則：

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

否則，`req=img`

## 另請參閱 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ，屬 [性：:ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [暈映：:UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85)，屬 [性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
