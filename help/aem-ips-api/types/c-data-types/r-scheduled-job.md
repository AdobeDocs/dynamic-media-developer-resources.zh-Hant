---
description: 計畫運行的作業。
solution: Experience Manager
title: 計畫作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 4%

---

# [!DNL ScheduledJob]{#scheduledjob}

計畫運行的作業。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 公司句柄 | `xsd:string` | 公司負責。 |
| 作業句柄 | `xsd:string` | 計畫的作業句柄。 |
| name | `xsd:string` | 工作名稱. |
| 原始名稱 | `xsd:string` | 計畫作業的原始名稱。 |
| type | `xsd:string` | 作業類型。 |
| 提交用戶電子郵件 | `xsd:string` | 調度作業的用戶的電子郵件地址。 |
| 地區設定 | `xsd:string` | 用於作業日誌詳細資訊和電子郵件本地化的區域設定。 區域設定指定為 `<language_code>[- <country_code>]`，其中，語言代碼是ISO-639指定的小寫雙字母代碼，可選國家代碼是ISO-3166指定的大寫雙字母代碼。 例如，英語（美國）的區域設定字串為： `en-US`。 |
| description | `xsd:string` | 最初在中指定的作業說明 `submitJob`。 |
| 執行計畫 | `xsd:string` | 作業計畫運行時間。 |
| 下一次火災時間 | `xsd:dateTime` | 觸發作業的日期、時間和時區。 |
| 時區 | `xsd:dateTime` | 計畫作業的時區。 |
| 觸發器狀態 | `xsd:int` | 作業觸發器狀態的選擇。 |
| imageServingPublishJob | `types:ImageServingPublishJob` | 提供發佈作業的映像的作業詳細資訊。 |
| imageServingRenderJob | `types:ImageServingRenderJob` | 影像呈現作業的作業詳細資訊。 |
| videoPublishJob | `types:VideoPublishJob` | 視頻發佈作業的作業詳細資訊。 請參閱 [視頻發佈工作](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |
| 伺服器目錄發佈作業 | `types:ServerDirectoryPublishJob` | 伺服器目錄發佈作業的作業詳細資訊。 |
| uploadDirectory作業 | `types:UploadDirectoryJob` | 上載目錄作業的作業詳細資訊。 |
| 上載Urls作業 | `types:UploadUrlsJob` | 上載URL作業的作業詳細資訊。 |
| 優化ImagesJob | `types:OptimizeImagesJob` |  |
| ripPdf作業 | `types:RipPdfsJob` |  |
| reprocessAssetsJob | `types:ReprocessAssetsJob` |  |
| 導出作業 | `types:ExportJob` | 允許授權導出以前上載的檔案。 請參閱 [導出作業](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |

## 附註 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

在中指定作業類型值時 `submitJob`，系統將根據該類型返回作業。 可以返回以下作業：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
