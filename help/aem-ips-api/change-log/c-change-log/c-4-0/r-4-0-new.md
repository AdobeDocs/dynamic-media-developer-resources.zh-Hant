---
title: 新增與變更
description: 說明IPS API v4.0的新變更和實施變更。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# 新增與變更{#new-additions-and-changes}

說明IPS API v4.0的新變更和實施變更。

使用單獨的WSDL和結構描述名稱空間並排實作API版本。

* 舊版API： `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`。
* SPS 4.0版本： `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`。

已新增`PostScriptOptions/alpha`欄位。

已新增`VideoRootUrl`作業的`SwfRootUrl`和`getProperty`屬性。

已將選用的`appName`和`appVersion`引數新增至`authHeader`以追蹤呼叫應用程式。 已新增記錄至`ipsApiService.log`。

新增選用的`serviceUrl`引數至WSDL產生servlet。 此引數對於除錯代理程式非常有用。 例如： `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

已實作`getZipEntries`作業。

針對系統欄位條件實作搜尋範圍並輸入比較值。

新增`'Asset'`個資產型別字串常數，主要用於允許跨資產中繼資料欄位。

已實作`trashState`的`searchAssets`引數。

已實作`getAssetPublishHistory`作業。

新增選用的`faultHttpStatusCode` SOAP標頭，以在Flex中啟用錯誤處理。 若為Flex，請使用`<faultHttpStatusCode>200</faultHttpStatusCode>`。 錯誤回應的預設狀態碼為`500 (Internal Server Error)`。

新增從垃圾桶還原資產和從垃圾桶還原空白資產的操作。

實作CRUD作業。

已將啟用的旗標新增至`ImageMap`型別和`saveImageMap`作業。

新增對「最佳化剩餘檔案」工作的支援。

已新增大量發佈狀態更新的`setAssetsPublishState`。

已新增`ImageServingPublishSettings`、`getImageServingPublishSettings`、`setImageServingPublishSettings`。

已棄用`saveMetadataField`作業以支援新的`createMetadataField`和`updateMetadataField`作業。

已實作`deleteAssetsParam`批次刪除作業。

已實作`moveAssetsParam`批次移動作業。

已實作`deleteMetadataField`作業。

已實作`get/setImageRenderingPublishSettings`、`get/set/create/updateVignettePublishFormat`作業。

已實作`getAssetCounts`。

已新增對`setImageSetMembers`的支援，以便在`RenderSet`個資產中包含`ImageSet`個成員。

已新增`replaceImage`作業。

已新增`copyImage`作業。

已新增`setUrlModifier`、`urlModifier/urlPostApplyModifier`和`LayerViewInfo`的`TemplateInfo`作業和`WatermarkInfo`欄位。

已新增`createDerivedAsset`作業。 目前`ownerHandle`必須參考影像資產，而且型別可以是`AdjustedView`或`LayerView`。

已新增`createTemplate`作業。 呼叫以建立範本或浮水印資產。

IPS公司設定`CompanySettings`已移植到網站服務API。

已新增`excludeByproducts`篩選器標幟至`searchAssets`作業。 將此標幟設為true會執行`PSDlayer`個影像和PDF擷取的影像。

已新增`getGenerationInfo`作業。

已新增`SystemMessage`屬性名稱至`getProperty`作業。

修改部分資產型別字串常數，以符合對應的資產資訊欄位。

* WordDoc： Word
* ExcelDoc： Excel
* PowerPointDoc： PowerPoint
* RTFDoc： Rtf

修改批次作業的結果格式，以彙總成功、警告和錯誤。

已實作`batchSetAssetMetadata`批次中繼資料作業。

實施應用程式特定資料的支援。

已針對上傳工作實作布林值標幟`createTemplate`、`extendLayers`和`extractText`的支援，以控制Photoshop處理的程式（類似於新增檔案上傳的變更）。

已實作`setImageMaps`和`setZoomTargets`作業。

已實作`ViewerPreset`作業。 可識別的型別為：

* `VideoPlayer` （視訊只會發佈這些檢視器。）
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

檢視器外觀元素支援兩個引數： `skinFg`和`skinBg`。 後端程式碼會執行維持回溯相容性所需的所有處理。

已實作`getAssociatedAssets`作業。

新增`ReprocessAssets`工作型別，以允許重新處理先前上載的主要來源檔案，包括重新擷取PDF和重新最佳化影像。

已將`PropertySetType`欄位型別重新命名為`propertyType`。 此重新命名會影響`createPropertySetType`引數和`getPropertySetType/getPropertySetTypes`回應。

已實作`batchSetImageFields`作業以支援設定影像使用者資料和其他可編輯的影像欄位。

47將fileSize欄位新增至各種資產資訊型別：

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

已實作`getActivePublishContexts`作業。 此操作會傳回具有指定公司之使用中發佈伺服器的發佈內容名稱陣列。 目前的發佈內容名稱為：

* `ImageServing`
* `ImageRendering`
* `Video`

已實作`getSearchStrings`作業。 它會傳回指定資產的搜尋字串陣列。

新增工作的地區設定引數，以及設定API作業地區設定的機制。 地區設定字串的格式應為`<language_code>[-<country_code>]`。 語言代碼是如ISO-639所指定的小寫、雙字母代碼，而選用的國家/地區代碼是如ISO-3166所指定的大寫、雙字母代碼。

將選用的地區設定引數新增到`authHeader` SOAP標題以設定API操作的地區設定。 如果此引數不存在，則會使用HTTP標頭`Accept-Language`。 如果此標頭也不存在，則會使用IPS伺服器的預設地區設定。

新增強型別中繼資料欄位的get/set支援。

實作SOAP和HTTP標題對gzip回應控制的支援。

已新增`gzipResponse`標幟至`authHeader`。 如果不存在，則API會檢查HTTP `Accept-Encoding`標頭。

新增對searchAssets的支援，以搜尋強型別中繼資料欄位條件。

* 對於所有欄位型別，可以使用字串比較運運算元( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)傳遞值
* 對於布林欄位，可以使用`boolVal`作業傳遞`Equals`。
* 對於Int欄位，可以使用數值比較運運算元( `longVal`)傳遞`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`，或使用數值範圍運運算元( `minLong/maxLong`)傳遞`Between, NotBetween`。
* 對於Float欄位，可以使用數值比較運運算元( `doubleVal`)傳遞`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`，或使用數值範圍運運算元( `minDouble/maxDouble`)傳遞`Between, NotBetween`。
* 對於日期欄位，您可以使用數值比較運運算元( `dateVal`)傳遞`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`，或者您可以使用數值範圍運運算元( `Between, NotBetween`)傳遞minDate/maxDate。

已新增描述、`jobSubType`和`originalJobName`欄位至`JobLog`型別。

* `originalJobName`是提交給`submitJob`的工作名稱（沒有任何唯一性尾碼或後續工作名稱）。
* `jobSubType`僅由`ImageServingPublishJob`個工作使用（其中為`full`、`increment, fullwithsearch,`或`fulloverride`其中之一）。
* `description`是適用於所有工作型別的空字串，但最終包含摘要工作資訊，例如上傳路徑。

此外，`getJobLogs`和`getJobLogDetails`未同時包含下列欄位。 在舊版中，它們僅適用於`getJobLogDetails`。

* `endDate` （如果工作已完成）。
* `fileDuplicateCount` （先前一律為`0`與`getJobLogs`）
* `fileUpdateCount` （先前一律為`0`與`getJobLogs`並包含在`fileSuccessCount`中；現在會分割為個別欄位）。

已將assetHandle欄位新增至`JobLogDetail`型別。

已將選擇性描述引數新增至`submitJob`。 傳遞此引數以在`getScheduledJobs`、`getActiveJobs`和`getJobLogs`中擷取。

已棄用SKU系統欄位。 如果欄位作為`SystemFieldCondition`傳入`searchAssets`，則會忽略該欄位。

已新增`excludeAssetTypeArray`篩選器至`searchAssets`。

已新增`MaskInfo`型別至`Asset`。

新增IPS管理的資產型別：

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
   <td colname="col2"> <p>以.doc結尾的檔案使用Microsoft® Word檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>以.xls結尾之檔案的Microsoft® Excel檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>以.ppt結尾之檔案的Microsoft® PowerPoint檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>以.rtf結尾的上傳檔案的RTF檔案。 </p> </td> 
  </tr> 
 </tbody> 
</table>

已新增其他選項至`UploadDirectoryJob`和`UploadUrlsJob`，以獨立控制Postscript、Illustrator和PDF檔案的處理。 所有現有作業都會為三個處理管道的每個提供必要引數，以便它們能夠與今天完全一樣運作。 原始`PostScriptOptions`區塊是用來設定Illustrator和EPS/PS檔案的處理作業。 您可以選擇提供特定的檔案選項區塊，以指定處理。 變更清單包括：

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
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph">無</span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph">點陣化</span> （預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>僅管理資產，上傳時不會建立任何衍生工具。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>以指定的解析度和色域將EPS和PostScript檔案演算為影像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>選擇性. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;布林值&gt; </span> </p> </td> 
   <td colname="col4"> <p>將檔案點陣化成影像時生效。 如果以這種方式定義原始檔案來覆蓋標誌，則會建立透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">處理序</span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph">無</span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph">點陣化</span> （預設） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>僅管理資產，上傳時不會建立任何衍生工具。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>以指定的解析度和色域將檔案演算為影像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>點陣化解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>呈現的目標色域。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>選擇性. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>將檔案點陣化成影像時生效。 如果以這種方式定義原始檔案來建立重疊圖志，則建立透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">處理序</span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph">無</span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph">點陣化</span> （預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>僅管理資產，上傳時不會建立任何衍生工具。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>以指定的解析度和色域將檔案演算為影像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>點陣化解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>呈現的目標色域。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;布林值&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義在轉譯後是否將多頁PDF結合至eCatalog （預設為true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;布林值&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義是否將PDF中的字詞擷取到DB中，以便稍後提供給搜尋伺服器（預設為false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您也可以從`getScheduledJobs`查詢。

已修改`webservice.gzip.response`設定屬性以取得下列其中一個值：

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
   <td colname="col2"> <p>不使用gzip回應。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>只有在authHeader/gzipResponse為true時，才有Gzip回應。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip （如果authHeader/gzipResponse為true，或不存在gzipResponse標頭且HTTP Accept-Encoding標頭包含gzip）。 （預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>一律使用gzip回應，無論標頭值為何。 此值僅用於偵錯。 </p> </td> 
  </tr> 
 </tbody> 
</table>
