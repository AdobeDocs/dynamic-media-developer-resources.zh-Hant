---
description: 允許重新處理先前上傳的主要檔案的工作類型，包括重新轉譯PDF和重新最佳化影像。
solution: Experience Manager
title: ReprocessAssetsJob
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 5%

---

# ReprocessAssetsJob{#reprocessassetsjob}

允許重新處理先前上傳的主要檔案的工作類型，包括重新轉譯PDF和重新最佳化影像。

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
   <td colname="col3"> <p>檔案是否已標示為可發佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>控制覆寫時是否會保留現有資產的發佈狀態。 如果未設定，則使用公司預設設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>是否建立遮色片。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>控制任何現有作物定義的保留。 預設為 true。</p> <p>如果您提供manualCropOptions參數和對應的值，則無論preserveCrop值為何，新值（不包括0,0,0,0）都會套用至資產。</p><p>如果您<i>not</i>提供manualCropOptions參數，則會維持preserveCrop的值。 若為true，則會保留現有的preserveCrop值；若為false，則會移除preserveCrop值。</p><p>範例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt;310&lt;/right&gt;<br />    &lt;top&gt;160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動裁切選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>根據顏色自動裁切影像的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>根據透明度從影像邊緣移除空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>將Photoshop檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>用於將PostScript檔案上載到影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>上傳PDF檔案至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>A/V介質檔案選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>將Illustrator檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>可在上傳期間指定的選項。 此設定會影響上傳色彩的管理方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>要套用至上傳檔案的自動設定產生指令碼陣列。 </p> </td> 
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
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>是否僅上傳檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>檔案上傳位置的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上傳完成後，要執行之影像提供發佈工作的工作詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上傳完成後要執行之影像呈現發佈作業的作業詳細資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型： VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上傳完成後要執行之視訊發佈工作的工作詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>用於將InDesign檔案上載到映像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knoupBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ThrunkedBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>遮罩所選影像的背景。 這可讓您以主體影像外部的透明度，在其他圖層中覆蓋它們。 </p> <p>選填。 </p> <p>請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> TrunkupBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：銳利化遮色片選項</span> </p> </td> 
   <td colname="col3"> <p>用於在建立優化金字塔TIF檔案時控制遮色片設定的選項。 使用這些設定可幫助提高影像的清晰度。 </p> <p>請參閱<a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**附註**

`*CropOptions`的選擇包括：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

`*PublishJob`的選擇包括：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
