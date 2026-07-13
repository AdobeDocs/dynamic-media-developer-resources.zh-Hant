---
description: 排定要執行的工作。
solution: Experience Manager
title: 排定的工作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
TQID: 'https://experienceleague.adobe.com/OFG30nHlkuRT7HeNob0hkEfaygi8b2gNFEiu67LJBmU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 276
ht-degree: 3%

---

# [!DNL ScheduledJob]{#scheduledjob}

排定要執行的工作。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| companyHandle | `xsd:string` | 公司控制代碼。 |
| jobHandle | `xsd:string` | 排程的工作控制代碼。 |
| name | `xsd:string` | 工作名稱。 |
| 原始名稱 | `xsd:string` | 排程工作的原始名稱。 |
| type | `xsd:string` | 工作型別。 |
| submitUserEmail | `xsd:string` | 排程工作之使用者的電子郵件地址。 |
| 地區設定 | `xsd:string` | 用於工作記錄檔詳細資料和電子郵件本地化的地區設定。 地區設定指定為`<language_code>[- <country_code>]`，其中語言程式碼為ISO-639所指定的小寫雙字母程式碼，而選用的國家程式碼為ISO-3166所指定的大寫雙字母程式碼。 例如，英文（美國）的地區設定字串將是： `en-US`。 |
| description | `xsd:string` | `submitJob`中最初指定的工作描述。 |
| execSchedule | `xsd:string` | 排定執行工作的時間。 |
| nextFireTime | `xsd:dateTime` | 觸發工作的日期、時間和時區。 |
| 時區 | `xsd:dateTime` | 排程工作的時區。 |
| triggerState | `xsd:int` | 選擇工作觸發程式狀態。 |
| imageServingPublishJob | `types:ImageServingPublishJob` | 影像伺服發佈工作的工作詳細資訊。 |
| imageServingRenderJob | `types:ImageServingRenderJob` | 影像演算工作的工作詳細資訊。 |
| videopublishJob | `types:VideoPublishJob` | 視訊發佈工作的工作詳細資訊。 請參閱[VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | 伺服器目錄發佈工作的工作詳細資訊。 |
| uploaddirectoriejob | `types:UploadDirectoryJob` | 上載目錄工作的工作詳細資訊。 |
| uploadUrlsJob | `types:UploadUrlsJob` | 上傳URL工作的工作詳細資訊。 |
| optimizeImagesJob | `types:OptimizeImagesJob` | |
| ripPdfJob | `types:RipPdfsJob` | |
| 重新處理資產工作 | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | 允許授權匯出先前上載的檔案。 請參閱[匯出工作](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |

## 附註 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

當您在`submitJob`中指定工作型別值時，系統會根據該型別傳回工作。 可傳回下列作業：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

