---
description: 公司專屬組態設定。
solution: Experience Manager
title: 公司設定
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 2%

---

# 公司設定{#companysettings}

公司專屬組態設定。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`overwriteMode`*` | `xsd:string` | 確定是否以相同的基本影像名稱和副檔名覆蓋當前資料夾中的影像。 |
| `*`retainPublishState`*` | `xsd:boolean` | 指定上傳至IPS的替代影像是否應保留現有的「準備發佈」設定，或是否應如上傳所指定。 |
| `*`defaultSourceProfile`*` | `types:Asset` | 在添加CMYK影像檔案時，指定作為「使用預設顏色行為」的一部分自動應用的預設源顏色配置檔案(Cobated FOGRA27(ISO 126472:2004))。 |
| `*`defaultDisplayProfile`*` | `types:Asset` | 指定在添加CMYK影像檔案時，作為「使用預設顏色行為」的一部分自動應用的預設內部顏色配置檔案(US Web Cobated(SWOP)v2)。 |
| `*`iptcExifMappingXslt`*` | `types:Asset` | 將IPTC和EXIF影像標頭資料提取到IPS中時，需要將公司的內部欄位名稱轉換為用戶定義的欄位名稱。 為上載的影像確定XSL轉換表（預設為「不提取任何IPTC或EXIF欄位」）。 |
| `*`xmpMappingXslt`*` | `types:Asset` | 將XMP影像標題資料擷取至IPS時，需要將公司的內部欄位名稱轉換為使用者定義的欄位名稱。 為已上載的影像確定XSL翻譯表(預設為「不提取任何XMP欄位」)。 |
| `*`diskSpaceWarningMin`*` | `xsd:int` | 發出警告之前映像目錄可用磁碟空間的最小量。 |
| `*`emailPrashCleanupWarning`*` | `xsd:boolean` | 決定是否要先傳送電子郵件，才能自動刪除放入垃圾桶的項目。 |
| `*`javascriptUploadEnabled`*` | `types:Asset` | 判斷是否要上傳JavaScript檔案。 這是潛在的安全風險，因此請謹慎使用此選項。 |
