---
description: 說明IPS API v4.0的新變更和實作變更。
solution: Experience Manager
title: 新增和變更
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 2%

---

# 新增和變更{#new-additions-and-changes}

說明IPS API v4.0的新變更和實作變更。

以個別的WSDL和架構命名空間實作並排的API版本。

* 舊版API:`IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`。
* SPS 4.0版本：`IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`。

新增`PostScriptOptions/alpha`欄位。

為`getProperty`操作新增`VideoRootUrl`和`SwfRootUrl`屬性。

新增選用`appName`和`appVersion`參數至`authHeader`以追蹤呼叫應用程式。 將記錄新增至`ipsApiService.log`。

將選用的`serviceUrl`參數新增至WSDL產生servlet。 這對除錯代理特別有用。 例如︰`http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

已實施`getZipEntries`操作。

為系統欄位條件實作搜尋範圍和輸入比較值。

新增`'Asset'`資產類型字串常數，主要用於允許跨資產中繼資料欄位。

為`searchAssets`實作`trashState`參數。

已實施`getAssetPublishHistory`操作。

新增選用的`faultHttpStatusCode` SOAP標題，以啟用Flex中的錯誤處理。 若為Flex，請使用`<faultHttpStatusCode>200</faultHttpStatusCode>`。 故障響應的預設狀態代碼為`500 (Internal Server Error)`。

新增從清單還原資產和從清單中清除資產的作業。

實施CRUD操作。

為`ImageMap`類型和`saveImageMap`操作新增已啟用的標幟。

新增對「最佳化剩餘檔案」作業的支援。

新增`setAssetsPublishState`以進行大量發佈狀態更新。

新增`ImageServingPublishSettings`、`getImageServingPublishSettings`、`setImageServingPublishSettings`。

已棄用`saveMetadataField`操作，改用新的`createMetadataField`和`updateMetadataField`操作。

已實施`deleteAssetsParam`批次刪除操作。

已實施`moveAssetsParam`批移動操作。

已實施`deleteMetadataField`操作。

實作`get/setImageRenderingPublishSettings`、`get/set/create/updateVignettePublishFormat`操作。

已實作`getAssetCounts`。

新增`setImageSetMembers`在`ImageSet`資產中包含`RenderSet`成員的支援。

新增`replaceImage`操作。

新增`copyImage`操作。

新增`setUrlModifier`操作和`urlModifier/urlPostApplyModifier`欄位，以用於`LayerViewInfo`、`TemplateInfo`和`WatermarkInfo`。

新增`createDerivedAsset`操作。 目前，`ownerHandle`必須參考影像資產，類型可能為`AdjustedView`或`LayerView`。

新增`createTemplate`操作。 目前，這可呼叫來建立範本或浮水印資產。

將IPS公司設定`CompanySettings`移植到網站服務API。

將`excludeByproducts`篩選標幟新增至`searchAssets`操作。 將此標幟設為true會執行`PSDlayer`影像和PDF擷取影像。

新增`getGenerationInfo`操作。

將`SystemMessage`屬性名稱新增至`getProperty`操作。

已修改某些資產類型字串常數，以符合對應的「資產資訊」欄位。

* WordDoc:Word
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

修改批處理操作的結果格式，以匯總成功、警告和錯誤。

實作`batchSetAssetMetadata`批次中繼資料操作。

實作應用程式特定資料的支援。

已實作對`createTemplate`、`extendLayers`和`extractText`布林值標幟的支援，讓上傳作業可控制Photoshop處理程式（類似於新增檔案上傳的變更）。

實作`setImageMaps`和`setZoomTargets`操作。

已實施`ViewerPreset`操作。 識別的類型為：

* `VideoPlayer` （影片只會發佈這些檢視器。）
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

檢視器外觀支援兩個參數：`skinFg`和`skinBg`。 後端程式碼會執行維持回溯相容性所需的所有處理作業。

已實施`getAssociatedAssets`操作。

新增`ReprocessAssets`工作類型，允許重新處理先前上傳的主要來源檔案，包括重新轉譯PDF和重新最佳化影像。

將`PropertySetType`欄位類型重新命名為`propertyType`。 這會影響`createPropertySetType`參數和`getPropertySetType/getPropertySetTypes`回應。

實作`batchSetImageFields`操作，以支援設定影像使用者資料和其他可編輯的影像欄位。

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

已實施`getActivePublishContexts`操作。 此操作會傳回一組發佈內容名稱，其中包含指定公司的作用中發佈伺服器。 當前發佈上下文名稱為：

* `ImageServing`
* `ImageRendering`
* `Video`

已實施`getSearchStrings`操作。 它會傳回指定資產的搜尋字串陣列。

新增作業的地區設定參數，以及設定API作業地區設定的機制。 地區設定字串的格式應為`<language_code>[-<country_code>]`。 語言代碼是ISO-639指定的小寫雙字母代碼，可選國家代碼是ISO-3166指定的大寫雙字母代碼。

在`authHeader` SOAP標題中新增選用的地區設定參數，以設定API操作的地區設定。 如果此參數不存在，則將使用HTTP標題`Accept-Language`。 如果此標頭不存在，則使用IPS伺服器的預設區域設定。

新增強類型化中繼資料欄位的取得/設定支援。

為gzip回應控制實作SOAP和HTTP標題支援。

將`gzipResponse`標幟新增至`authHeader`。 如果不存在，API也會檢查HTTP `Accept-Encoding`標題。

新增對searchAssets的支援，以提供強制類型中繼資料欄位條件。

* 對於所有欄位類型，可以使用字串比較運算子(`Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)傳遞值
* 對於布林欄位，`boolVal`可以與`Equals` op一起傳遞。
* 對於Int欄位，`longVal`可以用數值比較運算子(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)傳遞，或者`minLong/maxLong`可以用數值範圍運算(`Between, NotBetween`)傳遞。
* 對於浮點欄位，`doubleVal`可以用數值比較運算子(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)傳遞，或者`minDouble/maxDouble`可以用數值範圍運算(`Between, NotBetween`)傳遞。
* 對於「日期」欄位，您可以使用數值比較運算子(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)傳遞`dateVal`，也可以使用數值範圍運算(`Between, NotBetween`)傳遞minDate/maxDate。

將說明、`jobSubType`及`originalJobName`欄位新增至`JobLog`類型。

* `originalJobName` 是提交到的作業名 `submitJob` 稱（沒有任何唯一性尾碼或後續作業名稱）。
* `jobSubType` 目前僅供作 `ImageServingPublishJob` 業使用(其中是、 `full` `increment, fullwithsearch,` 或 `fulloverride`之一)。
* `description` 是所有作業類型的目前空字串，但最終將包含摘要作業資訊，例如上傳路徑。

此外，`getJobLogs`和`getJobLogDetails`中不包含以下欄位。 在舊版中，它們只能搭配`getJobLogDetails`使用。

* `endDate` （如果作業已完成）。
* `fileDuplicateCount` (之前一 `0` 律為 `getJobLogs`)
* `fileUpdateCount` (先前一律 `0` 包含 `getJobLogs` 在中 `fileSuccessCount`;現在會分割為個別欄位)。

將assetHandle欄位新增至`JobLogDetail`類型。

將選用說明參數新增至`submitJob`。 這會在`getScheduledJobs`、`getActiveJobs`和`getJobLogs`中傳遞以供擷取。

已棄用SKU系統欄位。 如果欄位以`SystemFieldCondition`傳入`searchAssets`，則會忽略該欄位。

將`excludeAssetTypeArray`篩選器新增至`searchAssets`。

將`MaskInfo`類型新增至`Asset`。

新增資產類型，供IPS管理：

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
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>結尾為.doc的檔案的Microsoft Word文檔。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>結尾為.xls的檔案的Microsoft Excel文檔。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>結尾為.ppt的檔案的Microsoft PowerPoint文檔。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>RTF檔案，用於以.rtf結尾的檔案。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新增其他選項至`UploadDirectoryJob`和`UploadUrlsJob`，以獨立控制Postscript、Illustrator和PDF檔案的處理。 所有現有作業都會為3條處理管道的每條管道提供必要的參數，使它們可如今一般運作。 原始的`PostScriptOptions`塊用於設定Illustrator和EPS/PS檔案的處理。 可選擇提供特定檔案選項塊以指定處理。 變更清單包括：

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 過程 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> 無 </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 柵格 </span>化（預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>僅管理資產，不要在上傳時建立任何衍生工具。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>以規定的解析度和顏色空間將EPS和PostScript檔案渲染到影像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>選填。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>將檔案柵格化為影像時生效。 如果以此方式定義原始檔案以覆蓋標誌，則會建立透明的背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 過程 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 無 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 柵格 </span> 化（預設） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>僅管理資產，不要在上傳時建立任何衍生工具。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>以規定的解析度和顏色空間將檔案渲染到影像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 解析度  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>模擬解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 色域 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用於渲染的目標顏色空間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> α  </span> </p> <p>選填。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>將檔案柵格化為影像時生效。 如果以此方式定義原始檔案以建立覆蓋標誌，則建立透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 過程 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 無 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 柵格 </span> 化（預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>僅管理資產，不要在上傳時建立任何衍生工具。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>以規定的解析度和顏色空間將檔案渲染到影像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 解析度  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>模擬解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 色域 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用於渲染的目標顏色空間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義轉譯後是否要將多頁PDF合併為eCatalog（預設為true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義PDF中的字詞是否提取到資料庫中，以供稍後提供給搜尋伺服器（預設為false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您也可以從`getScheduledJobs`查詢。

已修改`webservice.gzip.response`配置屬性，以取得下列其中一個值：

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
   <td colname="col2"> <p>只有在authHeader/gzipResponse為true時，Gzip回應才會。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 接受 </span> </p> </td> 
   <td colname="col2"> <p>如果authHeader/gzipResponse為true，或沒有gzipResponse標頭，且HTTP Accept-Encoding標頭包含gzip，則Gzip會。 (預設). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始終 </span> </p> </td> 
   <td colname="col2"> <p>無論標題值為何，一律gzip回應。 此值僅用於偵錯用途。 </p> </td> 
  </tr> 
 </tbody> 
</table>
