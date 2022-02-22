---
title: 請求
description: 請求類型. 指定請求的資料類型。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 4%

---

# 請求{#req}

請求類型. 指定請求的資料類型。

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 調試 </span> </p> </td> 
  <td class="stentry"> <p>在調試模式下運行命令。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 內容 </span> </p> </td> 
  <td class="stentry"> <p>返回有關視圖中對象的資訊。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>運行命令並返回呈現的影像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 影像 </span> </p> </td> 
  <td class="stentry"> <p>返回指定視圖的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 地圖 </span> </p> </td> 
  <td class="stentry"> <p>返回嵌入在視頻中的影像映射資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> object </span> </p> </td> 
  <td class="stentry"> <p>運行命令，並將已遮蔽的渲染影像返回到當前對象選擇。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>運行命令並返回回復映像的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 用戶資料 </span> </p> </td> 
  <td class="stentry"> <p>返回的內容 <span class="codeph"> vignette::UserData </span>。 </p> </td> 
 </tr> 
</table>

除非在詳細說明中另有說明，否則伺服器將返回MIME類型的文本響應 &lt;text plain=&quot;&quot;>。

`debug`

執行指定的命令並返回呈現的影像。 如果出現錯誤，將返回錯誤和調試資訊，而不返回錯誤影像( `attribute::ErrorImagePath`)。

`contents`

返回視圖中對象層次的XML表示形式，包括所選對象屬性。 請求中的其他命令將被忽略。

`img`

執行指定的命令並返回呈現的影像。 應答資料格式和響應類型由 `fmt=`。

`imageprops`

返回在URL路徑中指定的視圖檔案或目錄條目的選定屬性。 請參閱 [屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 的子菜單。 請求中的其他命令將被忽略。 返回以下屬性：

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
   <td colname="col2"> <p>雙 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：到期 </span> 或預設的生存時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 影像.height </span> </p> </td> 
   <td colname="col2"> <p>整數 </p> </td> 
   <td colname="col3"> <p>全解析度高度（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.icc配置檔案 </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p>與此視頻關聯的配置檔案的名稱/說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>布林 </p> </td> 
   <td colname="col3"> <p>1，如果關聯的配置檔案嵌入到視圖中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>布林 </p> </td> 
   <td colname="col3"> <p>1（如果視頻嵌入路徑資料）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：修改量 </span> 或空。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>枚舉 </p> </td> 
   <td colname="col3"> <p>響應影像的像素類型；可能是「CMYK」、「RGB」或「BW」（對於灰度影像）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>真實 </p> </td> 
   <td colname="col3"> <p>dpi中的預設打印解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p>修改日期/時間(自 <span class="codeph"> 目錄：:TimeStamp </span> 或vignette檔案)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>整數 </p> </td> 
   <td colname="col3"> <p>全解析度寬度（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>字串 </p> </td> 
   <td colname="col3"> <p>Vignette名稱（根Vignette對象的名稱字串）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>真實 </p> </td> 
   <td colname="col3"> <p>最大對象解析度 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材料解析度 </a> 單位（通常為像素/英吋）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>真實 </p> </td> 
   <td colname="col3"> <p>中的平均對象解析度 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材料解析度 </a> 單位（通常為像素/單位） <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材料解析度 </a>h)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>真實 </p> </td> 
   <td colname="col3"> <p>中的最小對象解析度 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材料解析度 </a> 單位（通常為像素/英吋）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>整數 </p> </td> 
   <td colname="col3"> <p>Vignette檔案版本號。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

返回視頻中包含的影像映射資料。 預設情況下，返回所有最外面的組的映射資料。 可使用

`req=map&groupLevel=-1`

地圖資料未縮放到 `wid=` 或 `hei=` 或以其他方式修改。 響應MIME類型為 `<text/xml>`。

響應資料由 `<map>` 包含一組 `<area>` 元素，類似於HTML `<AREA>` 標籤。

每個 `<area>` 元素包括標準 `type=` 和 `coord=` 屬性和 `name=` 屬性，指定vignette組名或名稱路徑。 多重 `<area>` 如果相應對象組的蒙版具有不連續的區域，則存在同名的元素。

除了預設屬性外，如果創作了該屬性，小格還可以定義附加屬性。 此類自定義屬性定義為對象組屬性。 自定義屬性的名稱必須以開頭 `map` 將包括在 `<area>` 元素。 例如，如果組屬性包括 `map.href=http://www.scene7.com`，對應 `<area>` 元素 `href="http://www.scene7.com"`。

空的XML文檔 `<map>` 如果vignette不包含映射資料，則返回元素。

`object`

執行指定命令並返回由剩餘對象選擇（最後一個對象選定的組或對象）所掩蔽的渲染影像 `sel=` 或 `obj=` 命令)。 通常與支援Alpha的影像格式一起使用(請參見 [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c))。 如果使用不支援Alpha的影像格式，則蒙版外部的區域為黑色。

`props`

執行指定的命令並返回視圖屬性和組或對象屬性，而不是呈現的影像。 請參閱 [屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 的子菜單。 除非 `obj=` 或 `sel=` 也指定了(請參見 [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a))。

響應中可能包含以下屬性：

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
   <td> <p> <span class="codeph"> 影像.bgc </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 答復影像背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像.height </span> </p> </td> 
   <td> <p>整數 </p> </td> 
   <td> <p> 答復影像高度（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> 布林 </p> </td> 
   <td> <p>如果ICC配置檔案嵌入回復影像中，則為True(請參見 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.icc配置檔案 </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與回復影像關聯的配置檔案的快捷方式名稱(請參閱 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 布林 </p> </td> 
   <td> <p> 如果回復影像包含Alpha，則為True。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> 布林 </p> </td> 
   <td> <p> 如果回復影像包含路徑資料，則為True(請參見 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回復影像類型，可以是「CMYK」、「RGB」或「BW」（對於灰度影像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> 打印解析度(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像質量 </span> </p> </td> 
   <td> <p>整數，布爾 </p> </td> 
   <td> <p> JPEG質量和色度標誌(請參閱 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回復影像的Mime類型(請參見 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 答復影像寬度（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 選擇屬性 </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 當前所選內容的屬性字串。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 選擇。計數 </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前所選內容中的對象數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 縮進當前所選內容的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 選擇 <span class="codeph"> 選擇屬性 </span>ion.name </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 當前對象選擇的全名路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 選擇。重疊 </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前選定內容中的重疊對象數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p>當前所選內容中可呈現對象的數量。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.textable </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前所選內容中可文本化的對象數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前所選內容的當前顯示/隱藏狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 選擇.zorder </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 當前所選內容中第一個重疊對象的Z階值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

返回的內容 `vignette::UserData`。 伺服器將替換 `'??'` 在 `vignette::UserData` 使用行終結器( `<cr><lf>`)。 答復格式化為文本資料，響應MIME類型設定為 &lt;text plain=&quot;&quot;>。

如果在URL路徑中指定的對象未解析為有效的視圖映射條目，或 `vignette::UserData` 為空，答復將只包含行終結器( `CR/LF`)。

將忽略請求字串中的任何其他命令。

## 屬性 {#section-e44092e190ff4f6380583e8ed6ea5b0b}

請求命令。 可能在請求字串中的任何位置發生。

## 預設 {#section-00c593cbf1af4364b6b78812e6b93c64}

如果URL不包括影像路徑或修飾符，則：

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

否則， `req=img`

## 另請參閱 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) 。 [屬性：:ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)。 [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85)。 [屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
