---
description: 特定於公司的配置設定。
solution: Experience Manager
title: 公司設定
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

特定於公司的配置設定。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 覆蓋模式 | `xsd:string` | 確定是否覆蓋當前資料夾中具有相同基本影像名稱和副檔名的影像。 |
| 保留發佈狀態 | `xsd:boolean` | 指定上傳到IPS的替換映像是應保留現有的「準備發佈」設定，還是應按上載指定的方式進行。 |
| defaultSourceProfile | `types:Asset` | 指定在添加CMYK影像檔案時自動作為「使用預設顏色行為」的一部分應用的預設源顏色配置檔案(Cobited FOGRA27(ISO 126472:2004))。 |
| defaultDisplayProfile | `types:Asset` | 指定在添加CMYK影像檔案時自動作為「使用預設顏色行為」的一部分應用的預設內部顏色配置檔案(US Web Coptied(SWOP)v2)。 |
| iptcExifMappingXslt | `types:Asset` | 將IPTC和EXIF影像頭資料提取到IPS中需要將公司的內部欄位名轉換為用戶定義的欄位名。 確定上載影像的XSL轉換表（預設值為「不提取任何IPTC或EXIF欄位」）。 |
| xmpMappingXslt | `types:Asset` | 將影像XMP頭資料提取到IPS中需要將公司的內部欄位名轉換為用戶定義的欄位名。 確定上載影像的XSL轉換表(預設為「不提取任XMP何欄位」)。 |
| diskSpaceWarningMin | `xsd:int` | 發出警告之前映像目錄可用磁碟空間的最小量。 |
| emailTrashCleanupWarning | `xsd:boolean` | 確定是否在將項目放入垃圾箱中之前發送電子郵件。 |
| javascriptUploadEnabled | `types:Asset` | 確定是否上載JavaScript檔案。 這是潛在的安全風險，因此請謹慎使用此選項。 |
