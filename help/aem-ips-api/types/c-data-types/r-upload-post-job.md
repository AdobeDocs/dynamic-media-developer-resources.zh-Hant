---
description: 使用getActiveJobs來追蹤案頭上傳。
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 10%

---

# UploadPostJob{#uploadpostjob}

使用getActiveJobs來追蹤案頭上傳。

另請參閱[透過HTTP POST上傳資產至上傳……](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d)。

>[!NOTE]
>
>上傳作業的所有POST請求都必須源自相同的IP位址。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>必要? </p> </th> 
   <th colname="col4" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>根據顏色自動裁切影像的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>要套用至上傳檔案的自動設定產生指令碼陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>根據透明度從影像邊緣移除空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>可在上傳期間指定的選項。 此設定會影響上傳色彩的管理方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>是否建立遮色片。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>選擇電子郵件設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：InDesignOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用於將InDesign檔案上載到映像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：IllustratorOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>將Illustrator檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knoupBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ThrunkedBackgroundOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>遮罩所選影像的背景。 這可讓您以主體影像外部的透明度，在其他圖層中覆蓋它們。 選填。 </p> <p>請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> TrunkupBackgroundOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ManualCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>手動裁切影像的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：MediaOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>可讓您從影片設定縮圖影像的選項。 </p> <p>請參閱<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆寫</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>是</p> </td> 
   <td colname="col4"> <p>上傳時是否要覆寫檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PDFOptions</span> </td> 
   <td colname="col3"> <p>否</p> </td> 
   <td colname="col4"> <p>上傳PDF檔案至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>將Photoshop檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>上傳檔案的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PostScriptOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用於將Post指令碼檔案上載到影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>控制任何現有作物定義的保留。 預設為 true。</p> <p>如果您提供manualCropOptions參數和對應的值，則無論preserveCrop值為何，新值（不包括0,0,0,0）都會套用至資產。</p><p>如果您<i>not</i>提供manualCropOptions參數，則會維持preserveCrop的值。 若為true，則會保留現有的preserveCrop值；若為false，則會移除preserveCrop值。</p><p>範例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt;310&lt;/right&gt;<br />    &lt;top&gt;160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>控制覆寫時是否會保留現有資產的發佈狀態。 如果未設定，則使用公司預設設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：HandleArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>項目句柄的陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>檔案是否已標示為可發佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：UnCompressOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>使用這些選用設定來解壓縮及處理上傳之TAR/ZIP檔案的內容。 </p> <p>請參閱<a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：銳利化遮色片選項</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用於在建立優化金字塔TIF檔案時控制遮色片設定的選項。 使用這些設定可幫助提高影像的清晰度。 </p> <p>請參閱<a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>上傳工作中所有項目的其他中繼資料選項。 </p> </td> 
  </tr> 
 </tbody> 
</table>
