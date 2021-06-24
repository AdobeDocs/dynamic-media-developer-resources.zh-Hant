---
description: 從您要取得檔案的位置上傳URL。
solution: Experience Manager
title: UploadUrlsJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 28bca473-670f-4588-93fb-a6d6a692ce30
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 5%

---

# UploadUrlsJob{#uploadurlsjob}

從您要取得檔案的位置上傳URL。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AutoColorCropOptions</span> </td> 
   <td colname="col3"> 根據顏色自動裁切影像的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AutoSetCreationOptions</span> </td> 
   <td colname="col3"> 要套用至上傳檔案的自動設定產生指令碼陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> 根據透明度從影像邊緣移除空白。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是否建立遮色片。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ColorManagementOptions</span> </td> 
   <td colname="col3"> 可在上傳期間指定的選項。 此設定會影響上傳色彩的管理方式。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 選擇電子郵件設定。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：IllustratorOptions</span> </td> 
   <td colname="col3"> 將Illustrator檔案上傳至影像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：InDesignOptions</span> </td> 
   <td colname="col3"> 用於將InDesign檔案上載到伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knoupBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ThrunkedBackgroundOptions</span> </td> 
   <td colname="col3">遮罩所選影像的背景。 這可讓您以主體影像外部的透明度，在其他圖層中覆蓋它們。 選填。請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> TrunkupBackgroundOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ManualCropOptions</span> </td> 
   <td colname="col3"> 手動裁切影像的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：MediaOptions</span> </td> 
   <td colname="col3">可讓您從影片設定縮圖影像的選項。 請參閱<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">傳回在工作中提交的URL數。 由<a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a>和<a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>使用。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆寫</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 上傳時是否要覆寫檔案。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PDFOptions</span> </td> 
   <td colname="col3"> 上傳PDF檔案至影像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PhotoshopOptions</span> </td> 
   <td colname="col3"> 將Photoshop檔案上傳至影像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 上傳檔案的URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageRendingPublishJob</span> </td> 
   <td colname="col3"> 上傳完成後執行之影像呈現發佈工作的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 所有介質選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PostScriptOptions</span> </td> 
   <td colname="col3"> 用於將Post指令碼檔案上載到影像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型： VideoPublishJob</span> </td> 
   <td colname="col3"> 上傳完成後執行之視訊發佈工作的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 控制任何現有作物定義的保留。 預設為true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 控制覆寫時是否會保留現有資產的發佈狀態。 如果未設定，則使用公司預設設定。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：HandleArray</span> </td> 
   <td colname="col3"> 項目句柄的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 檔案是否已標示為可發佈。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：UnCompressOptions</span> </td> 
   <td colname="col3">使用這些選用設定來解壓縮及處理上傳之TAR/ZIP檔案的內容。 請參閱<a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：銳利化遮色片選項</span> </td> 
   <td colname="col3">用於在建立優化金字塔TIF檔案時控制遮色片設定的選項。 使用這些設定可幫助提高影像的清晰度。 請參閱<a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> 您要上傳的URL陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>上傳工作中所有項目的其他中繼資料選項。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 附註 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

對於`CropOptions`，您只能選擇以下選項之一：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

對於`PublishJob`，您只能選擇以下選項之一：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`
