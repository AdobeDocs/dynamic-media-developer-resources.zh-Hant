---
description: 說明IPS API v4.0的新變更和實作變更。
seo-description: 說明IPS API v4.0的新變更和實作變更。
seo-title: 新增和變更
solution: Experience Manager
title: 新增和變更
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 新增和變更{#new-additions-and-changes}

說明IPS API v4.0的新變更和實作變更。

使用個別的WSDL和架構名稱空間並排實作API版本。

* 舊版API: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`。
* SPS 4.0版： `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`。

新增欄 `PostScriptOptions/alpha` 位。

已新增 `VideoRootUrl` 和屬 `SwfRootUrl` 性以執行 `getProperty` 作業。

新增可選 `appName` 和參 `appVersion` 數以追 `authHeader` 蹤呼叫應用程式。 已新增記錄 `ipsApiService.log`至。

已新增選 `serviceUrl` 用參數至WSDL層代servlet。 這對於除錯Proxy特別有用。 例如︰`http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

已實施 `getZipEntries` 操作。

已實作系統欄位條件的搜尋範圍和輸入比較值。

新增 `'Asset'` 資產類型字串常數，主要用於允許跨資產中繼資料欄位。

實作 `trashState` 參數 `searchAssets`。

已實施 `getAssetPublishHistory` 操作。

新增可選 `faultHttpStatusCode` 的SOAP標題，以啟用Flex中的錯誤處理。 若是Flex，請使用 `<faultHttpStatusCode>200</faultHttpStatusCode>`。 故障響應的預設狀態代碼為 `500 (Internal Server Error)`。

已新增從垃圾筒還原資產和從垃圾筒清空資產的作業。

已實施CRUD操作。

已新增已啟用的標 `ImageMap` 幟至類型 `saveImageMap` 和作業。

新增對「最佳化剩餘檔案」工作的支援。

已新 `setAssetsPublishState` 增大量發佈狀態更新。

Added `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

不再 `saveMetadataField` 提倡新操作和 `createMetadataField` 操作 `updateMetadataField` 的操作。

已實施 `deleteAssetsParam` 批刪除操作。

已實施 `moveAssetsParam` 批移動操作。

已實施 `deleteMetadataField` 操作。

實施 `get/setImageRenderingPublishSettings`、 `get/set/create/updateVignettePublishFormat` 操作。

Implemented `getAssetCounts`.

已新增支援 `setImageSetMembers` 將成員包 `RenderSet` 含在資產 `ImageSet` 中。

已添加 `replaceImage` 操作。

已添加 `copyImage` 操作。

已新 `setUrlModifier` 增、 `urlModifier/urlPostApplyModifier` 和的 `LayerViewInfo`操作和 `TemplateInfo`欄位 `WatermarkInfo`。

已添加 `createDerivedAsset` 操作。 目前， `ownerHandle` 必須參考影像資產，且類型可能 `AdjustedView` 為或 `LayerView`。

已添加 `createTemplate` 操作。 目前可呼叫此項來建立範本或浮水印資產。

IPS公司設定， `CompanySettings`已移植至網站服務API。

已新增 `excludeByproducts` 篩選標幟至 `searchAssets` 操作。 將此標幟設為true會執行影 `PSDlayer` 像和PDF擷取的影像。

已添加 `getGenerationInfo` 操作。

已將屬 `SystemMessage` 性名稱添加到操 `getProperty` 作中。

已修改某些資產類型字串常數，以符合對應的「資產資訊」欄位。

* WordDoc:Word
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

修改了批次操作的結果格式，以匯總成功、警告和錯誤。

實作批 `batchSetAssetMetadata` 次中繼資料作業。

已實作應用程式特定資料的支援。

已實作對布林旗標的支 `createTemplate`援， `extendLayers`以及 `extractText` 上傳工作，以控制Photoshop處理程式（類似於新增檔案上傳的變更）。

實作 `setImageMaps` 與 `setZoomTargets` 運作。

已實施 `ViewerPreset` 操作。 識別的類型有：

* `VideoPlayer` （視訊僅發佈這些檢視器。）
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

檢視器外觀支援兩個參數： `skinFg` 和 `skinBg`。 後端程式碼將執行所有必要的處理，以維持回溯相容性。

已實施 `getAssociatedAssets` 操作。

已新 `ReprocessAssets` 增工作類型，可重新處理先前上傳的主檔案，包括重新轉存PDF和重新最佳化影像。

將欄 `PropertySetType` 位類型重新命名為 `propertyType`。 這會影響參 `createPropertySetType` 數和 `getPropertySetType/getPropertySetTypes` 回應。

實作 `batchSetImageFields` 操作以支援設定影像使用者資料和其他可編輯的影像欄位。

47將fileSize欄位新增至各種資產資訊類型：

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

已實施 `getActivePublishContexts` 操作。 此操作返回一組具有指定公司活動發佈伺服器的發佈上下文名稱。 目前的發佈內容名稱為：

* `ImageServing`
* `ImageRendering`
* `Video`

已實施 `getSearchStrings` 操作。 它會傳回指定資產的搜尋字串陣列。

已新增工作的地區設定參數，以及設定API作業地區設定的機制。 地區設定字串的格式應為 `<language_code>[-<country_code>]`。 語言代碼是ISO-639指定的小寫、雙字母代碼，而可選的國家代碼是ISO-3166指定的大寫、雙字母代碼。

在SOAP標題中新增選用的地區 `authHeader` 設定參數，以設定API作業的地區設定。 如果此參數不存在，則會使 `Accept-Language` 用HTTP標題。 如果此標題也不存在，則將使用IPS伺服器的預設區域設定。

新增對強式類型中繼資料欄位的取得／設定支援。

已實作SOAP和HTTP標頭支援gzip回應控制。

新增 `gzipResponse` 旗標至 `authHeader`。 如果它不存在，API也會檢查HTTP標 `Accept-Encoding` 題。

新增對searchAssets的強式型別中繼資料欄位條件支援。

* 對於所有欄位類型，值可以與字串比較運算元( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)一起傳遞
* 對於布爾欄位， `boolVal` 可以與op一起 `Equals` 傳遞。
* 對於Int欄位， `longVal` 可以用數字比較運算子( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)傳遞， `minLong/maxLong` 也可以用數字範圍運算( `Between, NotBetween`)傳遞。
* 對於「浮點」 `doubleVal` 欄位，可以使用數值比較運算元( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)傳遞， `minDouble/maxDouble` 或者可以使用數值範圍運算( `Between, NotBetween`)傳遞。
* 對於「日期」欄位，您可 `dateVal` 以使用數字比較運算子( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)傳遞，或者可以使用數字範圍運算子( `Between, NotBetween`)傳遞minDate/maxDate。

新增說明 `jobSubType`、欄位 `originalJobName` 和欄位 `JobLog` 至類型。

* `originalJobName` 是提交到的作業名 `submitJob` 稱（沒有任何唯一性尾碼或後續作業名稱）。
* `jobSubType` 目前僅供工 `ImageServingPublishJob` 作使用(其中是 `full`或 `increment, fullwithsearch,` 之一 `fulloverride`)。
* `description` 目前是所有作業類型的空字串，但最終將包含摘要作業資訊，例如上傳路徑。

此外，下列欄位不會同時包含在和 `getJobLogs` 中 `getJobLogDetails`。 在舊版中，它們僅提供 `getJobLogDetails`。

* `endDate` （如果工作完成）。
* `fileDuplicateCount` (以前一直都 `0` 有 `getJobLogs`)
* `fileUpdateCount` (以前一直 `0` 與 `getJobLogs` 併入 `fileSuccessCount`;現在會分割為個別欄位)。

已新增assetHandle欄位至 `JobLogDetail` 類型。

將可選說明參數新增至 `submitJob`。 這會傳遞至，以便 `getScheduledJobs`在、 `getActiveJobs`和中擷取 `getJobLogs`。

已停用SKU系統欄位。 如果欄位傳入為「至」，則會忽略 `SystemFieldCondition` 該欄 `searchAssets`位。

新增 `excludeAssetTypeArray` 篩選至 `searchAssets`。

已將類 `MaskInfo` 型添加到 `Asset`。

已新增資產類型供IPS管理：

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
   <td colname="col2"> <p>Microsoft Word檔案，適用於以。doc結尾的檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>適用於以。xls結尾的檔案的Microsoft Excel檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>適用於以。ppt結尾之檔案的Microsoft PowerPoint檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>RTF檔案，用於以。rtf結尾上傳的檔案。 </p> </td> 
  </tr> 
 </tbody> 
</table>

已新增其他選 `UploadDirectoryJob` 項， `UploadUrlsJob` 以個別控制Postscript、Illustrator和PDF檔案的處理。 所有現有作業將為3條處理管道中的每一條提供必要的參數，使它們能夠像現在一樣正常工作。 原始 `PostScriptOptions` 區塊用來設定Illustrator和EPS/PS檔案的處理。 或者，可以提供特定的檔案選項塊來指定處理。 變更清單包括：

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 過程 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> 無 </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 點陣 </span>化（預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>僅管理資產，上傳時不建立任何衍生工具。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>將EPS和PostScript檔案演算為影像，以指定的解析度和色域。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>選填。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>將檔案點陣化為影像時生效。 如果以此方式定義原始檔案以覆蓋標誌，則會建立透明的背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 過程 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 無 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 點陣 </span> 化（預設） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>僅管理資產，上傳時不建立任何衍生工具。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>以規定的解析度和色域將檔案演算成影像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 解析度 </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>點陣化解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 色域 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用於轉換的目標色域。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>選填。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>將檔案點陣化為影像時生效。 如果以此方式定義原始檔案以建立覆蓋標誌，請建立透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 過程 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 無 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 點陣 </span> 化（預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>僅管理資產，上傳時不建立任何衍生工具。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>以規定的解析度和色域將檔案演算成影像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 解析度 </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>點陣化解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 色域 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用於轉換的目標色域。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義在轉譯後是否將多頁PDF合併為eCatalog（預設為true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義PDF中的字詞是否提取到DB中，以便稍後提供給搜尋伺服器（預設為false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您也可以從中查詢 `getScheduledJobs`。

已修改 `webservice.gzip.response` configuration屬性，以取得下列值之一：

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 永不 </span> </p> </td> 
   <td colname="col2"> <p>請勿gzip回應。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>僅當authHeader/gzipResponse為true時，Gzip回應。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 接受 </span> </p> </td> 
   <td colname="col2"> <p>如果authHeader/gzipResponse為true，或者沒有gzipResponse標題且HTTP Accept-Encoding標題包含gzip，則Gzip為Gzip。 (預設). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始終 </span> </p> </td> 
   <td colname="col2"> <p>不論標題值為何，一律gzip回應。 此值僅用於除錯用途。 </p> </td> 
  </tr> 
 </tbody> 
</table>

