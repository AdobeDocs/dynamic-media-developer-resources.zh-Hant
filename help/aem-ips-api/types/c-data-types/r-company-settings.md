---
description: 公司特定組態設定。
solution: Experience Manager
title: 公司設定
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# CompanySettings{#companysettings}

公司特定組態設定。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`overwriteMode`*` | `xsd:string` | 判斷是否以相同的基本影像名稱和副檔名覆寫目前檔案夾中的影像。 |
| `*`retainPublishState`*` | `xsd:boolean` | 指定上傳至IPS的取代影像應保留現有的「準備發佈」設定，還是應如上傳所指定。 |
| `*`defaultSourceProfile`*` | `types:Asset` | 指定在新增CMYK影像檔時，自動套用預設來源色彩描述檔(Copated FOGRA27(ISO 126472:2004))，做為「使用預設色彩行為」的一部分。 |
| `*`defaultDisplayProfile`*` | `types:Asset` | 指定在新增CMYK影像檔時，自動套用預設內部色彩描述檔(US Web Coptaded(SWOP)v2)作為「使用預設色彩行為」的一部分。 |
| `*`iptcExifMappingXslt`*` | `types:Asset` | 將IPTC和EXIF影像標題資料擷取至IPS時，需要將公司的內部欄位名稱轉換為使用者定義的欄位名稱。 為上傳的影像決定XSL轉譯表（預設為「不擷取任何IPTC或EXIF欄位」）。 |
| `*`xmpMappingXslt`*` | `types:Asset` | 將影像標XMP頭資料擷取至IPS時，需要將公司的內部欄位名稱轉換為使用者定義的欄位名稱。 為上傳的影像決定XSL轉譯表(預設為「不擷取任XMP何欄位」)。 |
| `*`diskSpaceWarningMin`*` | `xsd:int` | 發出警告前映像目錄可用磁碟空間的最小量。 |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | 決定是否在將項目放入垃圾筒中之前傳送電子郵件。 |
| `*`javascriptUploadEnabled`*` | `types:Asset` | 判斷是否上傳JavaScript檔案。 這是潛在的安全風險，因此請謹慎使用此選項。 |

