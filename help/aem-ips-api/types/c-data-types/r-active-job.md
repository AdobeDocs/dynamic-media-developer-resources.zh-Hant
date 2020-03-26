---
description: 在伺服器上運行的作業。 此外，它也是排程工作的例項。
seo-description: 在伺服器上運行的作業。 此外，它也是排程工作的例項。
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ActiveJob{#activejob}

在伺服器上運行的作業。 此外，它也是排程工作的例項。

Job存在於3個狀態：

* 已排程執行。
* 目前正在執行。
* 已完成運行（並已將資訊寫入作業日誌）。

指定作業類型值以返回作業類型。 您可以傳回下列工作：

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
   <td colname="col1"> <span class="codeph"> 公 <span class="varname"> 司控制</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 為公司負責。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 處理工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 作業的唯一名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 原 <span class="varname"> 始名稱</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">隨作業提交 <span class="codeph"> 的ActiveJob</span> 類型的原始名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 類型</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 系統返回的作業類型選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 系統返回的活動作業狀態選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 排程工作之使用者的電子郵件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 地區設定</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">作業日誌詳細資訊和電子郵件本地化的區域設定。 <p>指定地區設 <span class="codeph"> 定為&lt;language_code&gt;[-&lt;country_code&gt;]</span>，其中語言代碼是由ISO-639指定的小寫、雙字母代碼，而選用的國家代碼是由ISO-3166指定的大寫、雙字母代碼。 例如，英文（美國）的地區設定字串為： <span class="codeph"> en-US</span>。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 說 <span class="varname"> 明</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">job description submitJob中最初指 <span class="codeph"> 定的作業</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 服 <span class="varname"> 務器名</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 運行作業的伺服器的名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 作用中工作的日期、時間和時區。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 總 <span class="varname"> 大小</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 作用中工作的總大小。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 進 <span class="varname"> 度</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 任務進度（即任務完成的距離）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 進 <span class="varname"> 度訊息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 描述作業進度的文字訊息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上 <span class="varname"> 次進度更新</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上次進度更新的日期、時間和時區。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> taskProgressArray <span class="varname"> (任務進度陣列</span> ) </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：TaskProgressArray</span> </td> 
   <td colname="col3"> 非同步任務進度資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 影像伺服發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageServingRenderJob</span> </td> 
   <td colname="col3"> 影像轉譯發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型： VideoPublishJob</span> </td> 
   <td colname="col3"> 視訊發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 伺服器目錄發佈作業的作業詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上 <span class="varname"> 傳UrlsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：UploadUrlsJob</span> </td> 
   <td colname="col3"> 上傳URL工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：RipPdfJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 最 <span class="varname"> 佳化ImagesJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 重 <span class="varname"> 新處理AssetsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上 <span class="varname"> 傳PostJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：UploadPostJob</span> </td> 
   <td colname="col3"> 工作詳細資料追蹤案頭上傳。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 匯出工作</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ExportJob</span> </td> 
   <td colname="col3">允許授權匯出先前上傳的檔案。 請參閱 <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exportjob.html" format="http" scope="external"> 匯出工作</a>。 </td> 
  </tr> 
 </tbody> 
</table>

