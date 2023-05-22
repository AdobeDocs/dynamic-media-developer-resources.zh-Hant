---
description: 作業類型，允許重新處理以前上載的主檔案，包括重新翻錄PDF和重新優化映像。
solution: Experience Manager
title: 重新處理AssetsJob
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 5%

---

# [!DNL ReprocessAssetsJob]{#reprocessassetsjob}

作業類型，允許重新處理以前上載的主檔案，包括重新翻錄PDF和重新優化映像。

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
   <td colname="col3"> <p>資產句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 就緒，發佈</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>檔案是否已標籤為準備發佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>控制覆蓋時是否保留現有資產的發佈狀態。 如果未設定，則使用公司預設設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 建立掩碼</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>是否建立蒙版。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>控制對任何現有作物定義的保留。 預設為 true。</p> <p>如果提供manualCropOptions參數和相應值，則新值（不包括0,0,0,0）將應用於資產，而與preserveCrop值無關。</p><p>如果是 <i>不</i> 提供manualCropOptions參數，則保留preserveCrop的值。 並且，如果為true，則保留現有preserveCrop值；如果為false，則刪除preserveCrop值。</p><p>範例：</p><p><p>&lt;preservecrop&gt;假&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動裁剪選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 自動顏色裁剪選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>用於基於顏色的影像自動作物的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>根據透明度從影像邊緣刪除空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshop選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>用於將Photoshop檔案上載到映像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScript選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>用於將PostScript檔案上載到映像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdf選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>用於將PDF檔案上載到映像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 媒體選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：媒體選項</span> </p> </td> 
   <td colname="col3"> <p>A/V介質檔案選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustrator選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>用於將Illustrator檔案上載到映像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 顏色管理選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>可在上載過程中指定的選項。 該集會影響對上載顏色的管理方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 自動設定建立選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：自動設定建立選項</span> </p> </td> 
   <td colname="col3"> <p>要應用於上載檔案的自動集生成指令碼的陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>一組項目句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 電子郵件設定</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>電子郵件設定選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>是否僅上載檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>檔案上載位置的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上載完成後要運行的提供發佈作業的映像的作業詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上載完成後要運行的映像呈現發佈作業的作業詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上載完成後要運行的視頻發佈作業的作業詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 在設計選項中</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：InDesign選項</span> </p> </td> 
   <td colname="col3"> <p>用於將InDesign檔案上載到映像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 挖空背景</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：KnowBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>遮蔽選定影像的背景。 這樣，您就可以將它們疊加到主題影像之外具有透明度的其它圖層中。 </p> <p>選擇性. </p> <p>請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 挖空背景選項</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMask選項</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>用於在建立優化金字塔TIF檔案時控制非銳化蒙版設定的選項。 使用這些設定可幫助提高影像清晰度。 </p> <p>請參閱 <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMask選項</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**附註**

選擇 `*CropOptions` 包括：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

選擇 `*PublishJob` 包括：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
