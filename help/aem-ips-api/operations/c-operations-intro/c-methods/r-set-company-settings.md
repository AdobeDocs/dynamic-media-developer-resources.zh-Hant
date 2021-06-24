---
description: 設定各種公司專屬的設定值。
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# setCompanySettings{#setcompanysettings}

設定各種公司專屬的設定值。

語法

## 授權的使用者類型 {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-a472da6c57c74a94a179dda081004888}

**輸入(setCompanySettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`overwriteMode`*` | `xsd:string` | 否 | 資產覆寫模式。 |
| `*`retainPublishState`*` | `xsd:boolean` | 否 | 設為`true`以在重新上傳資產時保留發佈狀態。 |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | 否 | IccProfile資產，用作預設源顏色配置檔案。 |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | 否 | IccProfile資產，用作預設顯示顏色配置檔案。 |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | 否 | 用於將IPTC和EXIF元資料映射到IPS元資料欄位的XSL資產。 |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | 否 | 用於將XMP中繼資料對應至IPS中繼資料欄位的XSL資產。 |
| `*`diskSpaceWarningMin`*` | `xsd:int` | 否 | 發送警告消息之前可用的最小可用磁碟空間(KB)。 |
| `*`emailPrashCleanupWarning`*` | `xsd:boolean` | 否 | 設為`true` ，以便在資產從垃圾桶清空時，向公司管理員傳送通知。 |

**輸出(setCompanySettingsReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

此程式碼範例會設定公司的設定。

**請求**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**回答**

無。
