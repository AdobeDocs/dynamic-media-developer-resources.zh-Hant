---
title: 新增和更改
description: 介紹IPS API v4.0的新更改和已實現的更改。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 2%

---

# 新增和更改{#new-additions-and-changes}

介紹IPS API v4.0的新更改和已實現的更改。

使用單獨的WSDL和架構命名空間實現了並排API版本。

* 以前的API版本： `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`。
* SPS 4.0版本： `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`。

已添加 `PostScriptOptions/alpha` 的子菜單。

已添加 `VideoRootUrl` 和 `SwfRootUrl` 屬性 `getProperty` 的下界。

添加可選 `appName` 和 `appVersion` params `authHeader` 跟蹤調用的應用程式。 已將日誌記錄添加到 `ipsApiService.log`。

添加可選 `serviceUrl` 參數到WSDL層代servlet。 此參數對調試代理有用。 例如︰`http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

已實施 `getZipEntries` 的下界。

系統欄位條件的已實現搜索範圍和鍵入的比較值。

已添加 `'Asset'` 資產類型字串常數，主要用於允許跨資產元資料欄位。

已實施 `trashState` 參數 `searchAssets`。

已實施 `getAssetPublishHistory` 的下界。

添加可選 `faultHttpStatusCode` SOAP標頭，用於在Flex啟用故障處理。 對於Flex，使用 `<faultHttpStatusCode>200</faultHttpStatusCode>`。 故障響應的預設狀態代碼為 `500 (Internal Server Error)`。

增加了從垃圾中恢復資產和從垃圾中清空資產的操作。

已實施CRUD操作。

已將啟用標誌添加到 `ImageMap` 類型和 `saveImageMap` 的下界。

已添加對優化剩餘檔案作業的支援。

已添加 `setAssetsPublishState` 批量發佈狀態更新。

已添加 `ImageServingPublishSettings`。 `getImageServingPublishSettings`。 `setImageServingPublishSettings`。

已棄用 `saveMetadataField` 支援新的 `createMetadataField` 和 `updateMetadataField` 操作。

已實施 `deleteAssetsParam` 批刪除操作。

已實施 `moveAssetsParam` 批移動操作。

已實施 `deleteMetadataField` 的下界。

已實施 `get/setImageRenderingPublishSettings`。 `get/set/create/updateVignettePublishFormat` 操作。

已實施 `getAssetCounts`。

已添加對 `setImageSetMembers` 包括 `RenderSet` 成員 `ImageSet` 資產。

已添加 `replaceImage` 的下界。

已添加 `copyImage` 的下界。

已添加 `setUrlModifier` 操作和 `urlModifier/urlPostApplyModifier` 欄位 `LayerViewInfo`。 `TemplateInfo`, `WatermarkInfo`。

已添加 `createDerivedAsset` 的下界。 當前 `ownerHandle` 必須引用影像資產，類型可能 `AdjustedView` 或 `LayerView`。

已添加 `createTemplate` 的下界。 調用以建立模板或水印資產。

IPS公司設定， `CompanySettings`，已移植到Web服務API。

已添加 `excludeByproducts` 篩選器標誌 `searchAssets` 的下界。 將此標誌設定為true運行 `PSDlayer` 影像和PDF撕裂影像。

已添加 `getGenerationInfo` 的下界。

已添加 `SystemMessage` 屬性名稱 `getProperty` 的下界。

已修改某些資產類型字串常數以匹配相應的「資產資訊」欄位。

* WordDoc:字
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

修改了批處理操作的結果格式，以匯總成功、警告和錯誤。

已實施 `batchSetAssetMetadata` 批處理元資料操作。

已實施對特定於應用的資料的支援。

已實現對的布爾標誌的支援 `createTemplate`。 `extendLayers`, `extractText` 用於上載作業以控制Photoshop處理的進程（類似於添加檔案上載的更改）。

已實施 `setImageMaps` 和 `setZoomTargets` 操作。

已實施 `ViewerPreset` 操作。 識別的類型包括：

* `VideoPlayer` （視頻僅發佈這些查看者。）
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

查看器外觀支援兩個參數： `skinFg` 和 `skinBg`。 後端代碼執行維護向後相容性所需的所有處理。

已實施 `getAssociatedAssets` 的下界。

已添加 `ReprocessAssets` 作業類型，允許重新處理以前上載的主源檔案，包括重新翻錄PDF和重新優化映像。

已更名 `PropertySetType` 欄位類型 `propertyType`。 此更名會影響 `createPropertySetType` 參數和 `getPropertySetType/getPropertySetTypes` 回應。

已實施 `batchSetImageFields` 操作，以支援設定影像用戶資料和其他可編輯的影像欄位。

47將fileSize欄位添加到各種資產資訊類型：

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

已實施 `getActivePublishContexts` 的下界。 此操作將返回一組具有指定公司的活動發佈伺服器的發佈上下文名稱。 當前發佈上下文名稱為：

* `ImageServing`
* `ImageRendering`
* `Video`

已實施 `getSearchStrings` 的下界。 它返回給定資產的搜索字串陣列。

已添加作業的區域設定參數和設定API操作的區域設定的機制。 區域設定字串的格式應為 `<language_code>[-<country_code>]`。 語言代碼是ISO-639指定的小寫雙字母代碼，可選國家代碼是ISO-3166指定的大寫雙字母代碼。

將可選區域設定參數添加到 `authHeader` SOAP標頭，用於設定API操作的區域設定。 如果此參數不存在，則HTTP標頭 `Accept-Language` 的子菜單。 如果此標頭不存在，則使用IPS伺服器的預設區域設定。

已添加對強類型元資料欄位的獲取/集支援。

已實現SOAP和HTTP頭對gzip響應控制的支援。

已添加 `gzipResponse` 標籤 `authHeader`。 如果不存在，API將檢查HTTP `Accept-Encoding` 標題。

為searchAssets添加了對強類型元資料欄位條件的支援。

* 對於所有欄位類型，可以使用字串比較運算子傳遞值( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* 對於布爾欄位， `boolVal` 可能會與 `Equals` 行動。
* 對於Int欄位， `longVal` 可以用數字比較運算子傳遞( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)或 `minLong/maxLong` 可以通過數字範圍操作( `Between, NotBetween`)。
* 對於「浮點」欄位， `doubleVal` 可以用數字比較運算子傳遞( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)或 `minDouble/maxDouble` 可以通過數字範圍操作( `Between, NotBetween`)。
* 對於「日期」欄位，您可以通過 `dateVal` 具有數字比較運算子( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)，或者可以傳遞minDate/maxDate，其中包含數字範圍操作( `Between, NotBetween`)。

添加的說明， `jobSubType`, `originalJobName` 欄位 `JobLog` 的雙曲餘切值。

* `originalJobName` 是提交到的作業名稱 `submitJob` （沒有任何唯一性尾碼或後續作業名稱）。
* `jobSubType` 僅由 `ImageServingPublishJob` 工作(其中 `full`。 `increment, fullwithsearch,` 或 `fulloverride`)。
* `description` 是所有作業類型的空字串，但最終包含摘要作業資訊，如上載路徑。

此外，以下欄位不包括在兩者中 `getJobLogs` 和 `getJobLogDetails`。 在以前版本中，它們僅與 `getJobLogDetails`。

* `endDate` （如果作業已完成）。
* `fileDuplicateCount` (以前一直 `0` 與 `getJobLogs`)
* `fileUpdateCount` (以前一直 `0` 與 `getJobLogs` 和 `fileSuccessCount`;它現在被分割成單獨的欄位)。

已將assetHandle欄位添加到 `JobLogDetail` 的雙曲餘切值。

將可選說明參數添加到 `submitJob`。 此參數將傳遞到中以進行檢索 `getScheduledJobs`。 `getActiveJobs`, `getJobLogs`。

已棄用SKU系統欄位。 如果欄位作為 `SystemFieldCondition` 至 `searchAssets`。

已添加 `excludeAssetTypeArray` 篩選 `searchAssets`。

已添加 `MaskInfo` 類型 `Asset`。

已添加新的資產類型，以便按IPS管理：

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>資產類型 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Adobe Illustrator檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS和PostScript檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Word文檔，以.doc結尾的檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Excel文檔 </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Excel文檔，用於以.xls結尾的檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® PowerPoint文檔，以.ppt結尾的檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>以.rtf結尾的上載檔案的RTF檔案。 </p> </td> 
  </tr> 
 </tbody> 
</table>

添加了其他選項 `UploadDirectoryJob` 和 `UploadUrlsJob` 獨立控制Postscript、Illustrator和PDF檔案的處理。 所有現有作業都為三個處理管道中的每一個提供必要的參數，以便它們能夠像今天那樣正常工作。 原始 `PostScriptOptions` 塊用於設定Illustrator和EPS/PS檔案的處理。 可選地，可以提供特定檔案選項塊以指定處理。 更改清單包括：

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>欄位 </p> </th> 
   <th colname="col2" class="entry"> <p>參數 </p> </th> 
   <th colname="col3" class="entry"> <p>值 </p> </th> 
   <th colname="col4" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> 無 </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 光柵化 </span>（預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>僅管理資產，並且上載時不建立任何衍生項。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>將EPS和PostScript檔案以規定的解析度和顏色空間渲染到影像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>選擇性. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>將檔案柵格化為影像時生效。 如果以這種方式定義原始檔案以覆蓋徽標，則建立透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 過程 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 無 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 光柵化 </span> （預設） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>僅管理資產，並且上載時不建立任何衍生項。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>以規定的解析度和顏色空間將檔案渲染到影像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>光柵化解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用於渲染的目標顏色空間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>選擇性. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>將檔案柵格化為影像時生效。 如果以此方式定義原始檔案以建立重疊徽標，則建立透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOption </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 過程 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 無 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 光柵化 </span> （預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>僅管理資產，並且上載時不建立任何衍生項。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>以規定的解析度和顏色空間將檔案渲染到影像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>光柵化解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用於渲染的目標顏色空間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdf目錄 </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義在呈現後是否將多頁PDF組合到eCatalog（預設值為true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 抽取搜索詞 </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義是否將PDF中的字詞提取到資料庫中，以供以後提供給搜索伺服器（預設值為false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您也可以從 `getScheduledJobs`。

已修改 `webservice.gzip.response` configuration屬性，以獲取以下值之一：

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>不要進行gzip響應。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>僅當authHeader/gzipResponse為true時，Gzip響應才會出現。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>如果authHeader/gzipResponse為true，或者沒有gzipResponse標頭，並且HTTP Accept-Encoding標頭包含gzip，則Gzip。 (預設). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>始終gzip響應，而不考慮標頭值。 此值僅用於調試。 </p> </td> 
  </tr> 
 </tbody> 
</table>
