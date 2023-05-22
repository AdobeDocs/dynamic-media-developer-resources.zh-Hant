---
description: 從要獲取檔案的位置上載URL。
solution: Experience Manager
title: 上載Urls作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 28bca473-670f-4588-93fb-a6d6a692ce30
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 5%

---

# [!DNL UploadUrlsJob]{#uploadurlsjob}

從要獲取檔案的位置上載URL。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 自動顏色裁剪選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AutoColorCropOptions</span> </td> 
   <td colname="col3"> 用於基於顏色的影像自動作物的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 自動設定建立選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：自動設定建立選項</span> </td> 
   <td colname="col3"> 要應用於上載檔案的自動集生成指令碼的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> 根據透明度從影像邊緣刪除空白。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 建立掩碼</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是否建立蒙版。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 顏色管理選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ColorManagementOptions</span> </td> 
   <td colname="col3"> 可在上載過程中指定的選項。 該集會影響對上載顏色的管理方式。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 電子郵件設定</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 選擇電子郵件設定。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Illustrator選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：IllustratorOptions</span> </td> 
   <td colname="col3"> 用於將Illustrator檔案上載到映像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 在設計選項中</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：InDesign選項</span> </td> 
   <td colname="col3"> 用於將InDesign檔案上載到伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 挖空背景</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：KnowBackgroundOptions</span> </td> 
   <td colname="col3">遮蔽選定影像的背景。 這樣，您就可以將它們疊加到主題影像之外具有透明度的其它圖層中。 選擇性. 請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 挖空背景選項</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ManualCropOptions</span> </td> 
   <td colname="col3"> 手動作物影像的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 媒體選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：媒體選項</span> </td> 
   <td colname="col3">用於從視頻中設定縮略圖的選項。 請參閱 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 媒體選項</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 數字Url</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">返回作業中提交的URL數。 使用者 <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a> 和 <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆蓋</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 上載時是否覆蓋檔案。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdf選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PDFOptions</span> </td> 
   <td colname="col3"> 用於將PDF檔案上載到映像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshop選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PhotoshopOptions</span> </td> 
   <td colname="col3"> 用於將Photoshop檔案上載到映像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 上載檔案的URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageRendingPublishJob</span> </td> 
   <td colname="col3"> 上載完成後運行的影像呈現發佈作業的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 所有介質選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScript選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PostScriptOptions</span> </td> 
   <td colname="col3"> 用於將後指令碼檔案上載到映像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：VideoPublishJob</span> </td> 
   <td colname="col3"> 上載完成後運行的視頻發佈作業的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 控制對任何現有作物定義的保留。 預設為true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 控制覆蓋時是否保留現有資產的發佈狀態。 如果未設定，則使用公司預設設定。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：HandleArray</span> </td> 
   <td colname="col3"> 項目句柄陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 就緒，發佈</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 檔案是否已標籤為準備發佈。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：UnCompressOptions</span> </td> 
   <td colname="col3">使用這些可選設定提取並處理上載的TAR/ZIP檔案的內容。 請參閱 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> 取消壓縮選項</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMask選項</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：UnsharpMaskOptions</span> </td> 
   <td colname="col3">用於在建立優化金字塔TIF檔案時控制非銳化蒙版設定的選項。 使用這些設定可幫助提高影像清晰度。 請參閱 <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMask選項</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> url陣列</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> 要上載的URL陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmp關鍵字</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>上載作業中所有內容的附加元資料選項。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 附註 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

對於 `CropOptions`，您只能選擇以下選項之一：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

對於 `PublishJob`，您只能選擇以下選項之一：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`
