---
title: 需要
description: 請求型別。 指定要求的資料型別。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 3%

---

# 需要{#req}

請求型別。 指定要求的資料型別。

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">偵錯</span> </p> </td> 
  <td class="stentry"> <p>在偵錯模式下執行命令。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">內容</span> </p> </td> 
  <td class="stentry"> <p>傳回暈映中物件的相關資訊。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>執行命令並傳回演算後的影像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>傳回指定暈映的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">對應</span> </p> </td> 
  <td class="stentry"> <p>傳回內嵌在暈映中的影像地圖資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">物件</span> </p> </td> 
  <td class="stentry"> <p>執行命令並將遮色片所呈現的影像傳回至目前的物件選取範圍。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> prop </span> </p> </td> 
  <td class="stentry"> <p>執行命令並傳回回覆影像的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">使用者資料</span> </p> </td> 
  <td class="stentry"> <p>傳回<span class="codeph">暈映：：UserData </span>的內容。 </p> </td> 
 </tr> 
</table>

除非在詳細描述中另有說明，否則伺服器會傳回MIME型別&lt;text/plain>的文字回應。

`debug`

執行指定的命令並傳回演算後的影像。 如果發生錯誤，會傳回錯誤和偵錯資訊，而非錯誤影像( `attribute::ErrorImagePath`)。

`contents`

傳回暈映中物件階層的XML表示法，包括選取的物件屬性。 會忽略請求中的其他命令。

`img`

執行指定的命令並傳回演算後的影像。 回覆資料格式和回應型別由`fmt=`決定。

`imageprops`

傳回URL路徑中所指定暈映檔案或目錄專案的選取屬性。 如需回覆語法和回應MIME型別的說明，請參閱[屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)。 會忽略請求中的其他命令。 系統會傳回下列屬性：

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
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>兩次 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">屬性：：到期</span>或預設存留時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>整數 </p> </td> 
   <td colname="col3"> <p>以畫素為單位的完整解析度高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p>與此暈映關聯的設定檔名稱/說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>布林值 </p> </td> 
   <td colname="col3"> <p>1 （如果相關聯的設定檔內嵌於暈映中）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>布林值 </p> </td> 
   <td colname="col3"> <p>1 （如果暈映嵌入路徑資料）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">屬性：：修飾元</span>；若不是目錄專案，則為空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>列舉 </p> </td> 
   <td colname="col3"> <p>回應影像的畫素型別；可以是「CMYK」、「RGB」或「BW」（適用於灰階影像）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>實數 </p> </td> 
   <td colname="col3"> <p>以dpi為單位的預設列印解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p>修改日期/時間（來自<span class="codeph">目錄：：TimeStamp </span>或暈映檔案）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>整數 </p> </td> 
   <td colname="col3"> <p>以畫素為單位的完整解析度寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p>暈映名稱（根暈映物件的名稱字串）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>實數 </p> </td> 
   <td colname="col3"> <p>最大物件解析度<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">材質解析度</a>單位（通常是畫素/英吋）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>實數 </p> </td> 
   <td colname="col3"> <p>平均物件解析度<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">材質解析度</a>單位（通常是畫素/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">材質解析度</a>h）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>實數 </p> </td> 
   <td colname="col3"> <p>以<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local">材質解析度</a>單位（通常是畫素/英吋）為單位的最小物件解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>整數 </p> </td> 
   <td colname="col3"> <p>暈映檔案版本號碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

傳回暈映中包含的影像地圖資料。 依預設，會傳回所有最外層群組的對應資料。 可使用取得所有最內層群組的對應資料

`req=map&groupLevel=-1`

對應資料未縮放為`wid=`或`hei=`或以其他方式修改。 回應MIME型別為`<text/xml>`。

回應資料包含`<map>`元素，其中包含一組與HTML`<AREA>`標籤類似的`<area>`元素。

每個`<area>`元素都包含標準`type=`和`coord=`屬性，以及指定暈映群組名稱或名稱路徑的`name=`屬性。 如果對應物件群組的遮罩有不連續的區域，則存在多個同名的`<area>`元素。

除了預設屬性之外，如果已經創作，暈映可以定義其他屬性。 此類自訂屬性定義為物件群組屬性。 自訂屬性的名稱必須以`map`開頭，才能包含在`<area>`元素中。 例如，如果群組屬性包含`map.href=http://www.scene7.com`，則對應的`<area>`元素包含`href="http://www.scene7.com"`。

如果暈映不包含對應資料，則傳回含有空白`<map>`專案的XML檔案。

`object`

執行指定的命令，並傳回由剩餘物件選取範圍（要求中最後`sel=`或`obj=`命令選取的群組或物件）遮罩的演算影像。 通常搭配支援Alpha的影像格式使用（請參閱[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)）。 如果使用不支援Alpha的影像格式，遮色片外的區域為黑色。

`props`

執行指定的命令並傳回暈映屬性和群組或物件屬性，而不是彩現的影像。 如需回覆語法和回應MIME型別的說明，請參閱[屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)。 除非同時指定`obj=`或`sel=`，否則會套用預設選取範圍（請參閱[`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)）。

回應中可能包含以下屬性：

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
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回覆影像背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>整數 </p> </td> 
   <td> <p> 回覆影像高度（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> 布林值 </p> </td> 
   <td> <p>如果ICC設定檔內嵌在回覆影像中，則為True （請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與回覆影像關聯之設定檔的捷徑名稱（請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 布林值 </p> </td> 
   <td> <p> 如果回覆影像包含Alpha，則為True。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> 布林值 </p> </td> 
   <td> <p> 如果回覆影像包含路徑資料，則為True （請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回覆影像型別，可以是'CMYK'、'RGB'或'BW' （適用於灰階影像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 實數 </p> </td> 
   <td> <p> 列印解析度(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>整數，布林值 </p> </td> 
   <td> <p> JPEG品質和色度旗標（請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回覆影像的MIME型別（請參閱<span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 回覆影像寬度（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">選取專案。屬性</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 目前選取範圍的屬性字串。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">選擇。計數</span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 目前選取範圍中的物件數目。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">選取範圍。縮排</span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 目前選取範圍的縮排值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">選取<span class="codeph">選取專案。屬性</span>ion.name </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 目前物件選取範圍的完整名稱路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">選取範圍。重疊</span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 目前選取範圍中的重疊物件數目。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">選取範圍。可轉譯</span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p>目前選取範圍中的可轉譯物件數目。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">選取範圍。可紋理化</span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 目前選取範圍中的可紋理物件數目。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">選取範圍。可見</span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 目前顯示/隱藏目前選取專案的狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 目前選取範圍中第一個重疊物件的Z順序值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

傳回`vignette::UserData`的內容。 伺服器會將`vignette::UserData`中`'??'`的所有相符專案取代為行終止元( `<cr><lf>`)。 會將回覆格式化為文字資料，並將回應MIME型別設為&lt;text/plain>。

如果URL路徑中指定的物件未解析為有效的暈映對應專案，或者`vignette::UserData`是空的，則回覆僅包含行終止元( `CR/LF`)。

會忽略請求字串中的任何其他命令。

## 屬性 {#section-e44092e190ff4f6380583e8ed6ea5b0b}

要求命令。 可能發生在請求字串中的任何位置。

## 預設 {#section-00c593cbf1af4364b6b78812e6b93c64}

如果URL不包含影像路徑或修飾元，則：

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

否則，`req=img`

## 另請參閱 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ， [attribute：：ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)， [暈映：：UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85)， [屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
