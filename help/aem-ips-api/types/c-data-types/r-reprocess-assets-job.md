---
description: 工作類型可允許重新處理先前上傳的主要檔案，包括重新轉存PDF和重新最佳化影像。
solution: Experience Manager
title: 重新處理AssetsJob
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 5%

---


# ReprocessAssetsJob{#reprocessassetsjob}

工作類型可允許重新處理先前上傳的主要檔案，包括重新轉存PDF和重新最佳化影像。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>資產控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>檔案是否已標示為可供發佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：布林值</span> </p> </td> 
   <td colname="col3"> <p>控制覆寫現有資產時是否保留其發佈狀態。 如果未設定，則會使用公司預設設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：布林值</span> </p> </td> 
   <td colname="col3"> <p>是否建立蒙版。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：布林值</span> </p> </td> 
   <td colname="col3"> <p>控制任何現有裁切定義的保留。 預設為 true。</p> <p>如果您提供manualCropOptions參數和對應值，則新值（不包括0,0,0,0）會套用至資產，而不論preserveCrop值為何。</p><p>如果您<i>not</i>提供manualCropOptions參數，則preserveCrop的值會維持不變。 而且，若為true，則會保留現有的preserveCrop值；若為false，則會移除preserveCrop值。</p><p>範例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt; &lt;/right&gt;<br />    &lt;top&gt;310&lt;/top&gt;<br />    &lt;bottom&gt;160120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動裁切選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>可根據顏色自動裁切影像的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>根據透明度，從影像邊緣移除空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>將Photoshop檔案上載到映像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>上傳PostScript檔案至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdf選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>將PDF檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>A/V介質檔案選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>將Illustrator檔案上載到映像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>可在上傳期間指定的選項。 此設定會影響上傳色彩的管理方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>套用至上傳檔案的自動設定產生指令碼陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>項目句柄的陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>電子郵件設定選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：布林值</span> </p> </td> 
   <td colname="col3"> <p>是否只上傳檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>檔案上傳位置的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上傳完成後要執行之影像伺服發佈工作的工作詳細資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>要在上載完成後運行的影像渲染發佈作業的作業詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型： VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>視訊發佈工作的工作詳細資訊，將在上傳完成後執行。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>將InDesign檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knouckBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ThrounkBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>遮色所選影像的背景。 這可讓您在主題影像外以透明度覆蓋其他圖層。 </p> <p>選填。 </p> <p>請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> ThunkloupBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>可讓您在建立最佳金字塔TIF檔案時控制遮色片銳利化設定的選項。 使用這些設定可協助改善影像的銳利度。 </p> <p>請參閱<a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**附註**

`*CropOptions`的選項包括：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

`*PublishJob`的選項包括：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

