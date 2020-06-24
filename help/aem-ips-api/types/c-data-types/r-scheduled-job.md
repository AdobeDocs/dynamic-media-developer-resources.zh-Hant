---
description: 排程要執行的工作。
seo-description: 排程要執行的工作。
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Scene7 Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 3%

---


# ScheduledJob{#scheduledjob}

排程要執行的工作。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 公司負責人。 |
| ` *`jobHandle`*` | `xsd:string` | 排程的工作處理。 |
| ` *`名稱`*` | `xsd:string` | 工作名稱. |
| ` *`originalName`*` | `xsd:string` | 排程工作的原始名稱。 |
| ` *`類型`*` | `xsd:string` | 作業類型。 |
| ` *`submitUserEmail`*` | `xsd:string` | 排程工作的使用者的電子郵件地址。 |
| ` *`地區設定`*` | `xsd:string` | 用於作業日誌詳細資訊和電子郵件本地化的地區設定。 地區設定會指 `<language_code>[- <country_code>]`定為，其中語言代碼是ISO-639所指定的小寫、雙字母代碼，而選用的國家代碼是ISO-3166所指定的大寫、雙字母代碼。 例如，英文（美國）的地區設定字串為： `en-US`. |
| ` *`描述`*` | `xsd:string` | 最初在中指定的作業說明 `submitJob`。 |
| ` *`execSchedule`*` | `xsd:string` | 排程作業執行的時間。 |
| ` *`nextFireTime`*` | `xsd:dateTime` | 將引發工作的日期、時間和時區。 |
| ` *`時區`*` | `xsd:dateTime` | 排程作業的時區。 |
| ` *`triggerState`*` | `xsd:int` | 作業觸發狀態的選擇。 |
| ` *`imageServingPublishJob`*` | `types:ImageServingPublishJob` | 影像伺服發佈工作的工作詳細資訊。 |
| ` *`imageServingRenderJob`*` | `types:ImageServingRenderJob` | 影像轉譯工作的工作詳細資訊。 |
| ` *`videoPublishJob`*` | `types:VideoPublishJob` | 視訊發佈工作的工作詳細資訊。 請參 [閱VideoPublishJob](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |
| ` *`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | 伺服器目錄發佈作業的作業詳細資訊。 |
| ` *`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | 上載目錄作業的作業詳細資訊。 |
| ` *`uploadUrlsJob`*` | `types:UploadUrlsJob` | 上傳URL工作的工作詳細資訊。 |
| ` *`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| ` *`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| ` *`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| ` *`exportJob`*` | `types:ExportJob` | 允許授權匯出先前上傳的檔案。 請參 [閱匯出工作](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |

## 附註 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

在中指定作業類型值時， `submitJob`系統會根據該類型傳回作業。 可傳回下列工作：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

