---
description: 公司專屬組態設定。
solution: Experience Manager
title: 公司設定
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

公司專屬組態設定。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| overwriteMode | `xsd:string` | 決定是否以相同的基本影像名稱和副檔名覆寫目前資料夾中的影像。 |
| retainPublishState | `xsd:boolean` | 指定上載至IPS的取代影像是否應保留現有的「發佈準備就緒」設定，或依照上載的指定。 |
| defaultSourceProfile | `types:Asset` | 指定增加CMYK影像檔時，作為「使用預設色彩行為」的一部分自動套用的預設來源色彩設定檔(Coated FOGRA27 (ISO 126472：2004))。 |
| defaultDisplayProfile | `types:Asset` | 指定增加CMYK影像檔時，作為「使用預設色彩行為」的一部分自動套用的預設內部色彩設定檔(U.S. Web Coated (SWOP) v2)。 |
| iptcExifMappingXslt | `types:Asset` | 將IPTC和EXIF影像標題資料擷取到IPS需要從內部欄位名稱轉換成公司的使用者定義欄位名稱。 決定已上傳影像的XSL轉譯表格（預設值為「不要擷取任何IPTC或EXIF欄位」）。 |
| xmpMappingXslt | `types:Asset` | 將XMP影像標題資料擷取至IPS需要從內部欄位名稱轉換為公司的使用者定義欄位名稱。 決定已上傳影像的XSL轉譯表格(預設值為「不要擷取任何XMP欄位」)。 |
| diskSpaceWarningMin | `xsd:int` | 發出警告之前的最小影像目錄可用磁碟空間。 |
| emailTrashCleanupWarning | `xsd:boolean` | 決定是否要在自動刪除垃圾桶專案之前傳送電子郵件。 |
| javascriptuploadenabled | `types:Asset` | 決定是否上傳JavaScript檔案。 此選項有潛在安全性風險，請謹慎使用。 |
