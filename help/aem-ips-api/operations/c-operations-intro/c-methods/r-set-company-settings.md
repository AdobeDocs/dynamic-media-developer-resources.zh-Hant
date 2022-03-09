---
description: 設定各種特定於公司的配置值。
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 12%

---

# setCompanySettings{#setcompanysettings}

設定各種特定於公司的配置值。

語法

## 授權用戶類型 {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-a472da6c57c74a94a179dda081004888}

**輸入(setCompanySettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| 覆蓋模式 | `xsd:string` | 否 | 資產覆蓋模式。 |
| 保留發佈狀態 | `xsd:boolean` | 否 | 設定為 `true` 以在重新上載資產時保留發佈狀態。 |
| defaultSourceProfileHandle | `xsd:string` | 否 | IccProfile資產用作預設源顏色配置檔案。 |
| defaultDisplayProfileHandle | `xsd:string` | 否 | IccProfile資產用作預設顯示顏色配置檔案。 |
| iptcExifMappingXsltHandle | `xsd:string` | 否 | 用於將IPTC和EXIF元資料映射到IPS元資料欄位的XSL資產。 |
| xmpMappingXsltHandle | `xsd:string` | 否 | 用於將元資料映射XMP到IPS元資料欄位的XSL資產。 |
| diskSpaceWarningMin | `xsd:int` | 否 | 在發送警告消息之前可用的最小可用磁碟空間(KB)。 |
| emailTrashCleanupWarning | `xsd:boolean` | 否 | 設定為 `true` 在資產從垃圾箱清空時向公司管理員發送通知。 |

**輸出(setCompanySettingsReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

此代碼示例設定公司的配置。

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
