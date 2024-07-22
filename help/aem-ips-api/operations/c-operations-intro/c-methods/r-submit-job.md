---
description: 將工作提交至系統。
solution: Experience Manager
title: submitjob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 7%

---

# submitjob{#submitjob}

將工作提交至系統。

語法

## 授權的使用者型別 {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-31a07dbccf964850883e817384499459}

**輸入(submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>必要 </p> </th> 
   <th colname="col4" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>公司控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">使用者控制代碼</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>對提交工作的使用者進行處理。 </p> <p> <p>注意：系統傳送電子郵件給<span class="codeph"> userHandle</span>所指定的使用者。 如果未提供<span class="codeph"> userHandle</span>，則送出工作的人員會收到電子郵件。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">工作名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>工作名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">地區設定</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>用於工作記錄檔詳細資料和電子郵件本地化的地區設定。 </p> <p>地區設定指定為<span class="codeph"> &lt;language_code&gt;</span>和<span class="codeph"> [&lt;country_code&gt;]</span>，其中語言代碼為ISO-639所指定的小寫雙字母代碼，而選用的國家代碼為ISO-3166所指定的大寫雙字母代碼。 例如，英文（美國）的地區設定字串將是： en-US。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>執行工作的日期和時間。 </p> <p>注意：提供請求的時區。 時區會調整為目標IPS伺服器的時區。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>決定執行工作的時間。 </p> <p> 可以是以循環方式執行工作的<span class="codeph"> cron</span>字串。 </p> <p>排程一律與伺服器的本機時區相關。 如需自訂排程格式，請參閱IPS檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">描述</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>工作說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ExportJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>匯出先前上載的檔案。 </p> <p>請參閱<a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>影像伺服發佈工作的詳細資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>影像演算發佈工作的詳細資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：VideoPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>視訊發佈工作的詳細資料。 </p> <p>請參閱<a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>伺服器目錄發佈工作的詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：UploadDirectoryJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>上載目錄工作的詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：UploadUrlsJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>上傳URL工作的詳細資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：OptimizeImagesJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdf作業</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：RipPdfJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ReprocessAssetsJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>使用自動化集合指令碼將資產清單處理為集合。 </p> <p>請參閱<a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(submitJobReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| jobHandle | `xsd:string` | 是 | 工作控制代碼。 |

## 範例 {#section-40ac77d14adf4588ba2575be6879b2d2}

此程式碼範例將影像伺服發佈工作提交至IPS並傳回工作控制代碼。 在請求中僅選擇一種工作型別。 因為`userHandle`已省略，所以會傳送電子郵件通知給送出工作的使用者。 此範例工作會立即執行，因為省略了`execTime`和`execSchedule`。

**要求**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**回應**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## 附註 {#section-0f3078e503a249aeb6f3d662a51f036a}

您最多可以指定`execTime`和`execSchedule`其中之一。 如果兩者皆未傳遞，工作就會立即執行。 您只能使用下列其中一項：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
