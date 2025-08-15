---
title: 作用中的工作
description: 在伺服器上執行的工作。 此外，它也是排程工作的例項。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3d878207-99e4-4c75-ab12-b38a37c82fb7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---

# [!DNL ActiveJob]{#activejob}

在伺服器上執行的工作。 此外，它也是排程工作的例項。

工作分為三種狀態：

* 已排定執行。
* 目前正在執行。
* 已完成執行（且已將資訊寫入工作記錄檔）。

若要傳回工作型別，請指定工作型別值。 您可以傳回下列工作：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## 參數 {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 公司處理。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">工作控制代碼</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 處理工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 工作的唯一名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">原始名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3">與工作一併提交的<span class="codeph"> ActiveJob</span>型別的原始名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">型別</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 系統傳回的工作型別選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">狀態</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 選擇系統傳回的現用工作狀態。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 排程工作之使用者的電子郵件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">地區設定</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3">工作記錄檔詳細資料和電子郵件本地化的地區設定。 <p>將地區設定指定為<span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>，其中語言代碼為ISO-639所指定的小寫雙字母代碼，而選用的國家代碼為ISO-3166所指定的大寫雙字母代碼。 例如，英文（美國）的地區設定字串是： <span class="codeph"> en-US</span>。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">描述</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3">工作描述原本指定於<span class="codeph"> submitJob</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 執行工作的伺服器名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 作用中工作的日期、時間和時區。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 作用中工作的總大小。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">進度</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> 工單進度（即工單接近完工的程度）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> 描述工作進度的文字訊息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 上次進度更新的日期、時間和時區。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：TaskProgressArray</span> </td> 
   <td colname="col3"> 非同步工作進度資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 影像伺服發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ImageServingRenderJob</span> </td> 
   <td colname="col3"> 影像呈現發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：VideoPublishJob</span> </td> 
   <td colname="col3"> 視訊發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 伺服器目錄發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：UploadUrlsJob</span> </td> 
   <td colname="col3"> 上傳URL工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdf作業</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：RipPdfJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：UploadPostJob</span> </td> 
   <td colname="col3"> 工作詳細資料，追蹤案頭上傳。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ExportJob</span> </td> 
   <td colname="col3">允許授權匯出先前上載的檔案。 請參閱<a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-exportjob.html" format="http" scope="external">匯出作業</a>。 </td> 
  </tr> 
 </tbody> 
</table>
