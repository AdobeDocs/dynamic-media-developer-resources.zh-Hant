---
description: 設定各種公司專屬的設定值。
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# setCompanySettings{#setcompanysettings}

設定各種公司專屬的設定值。

語法

## 授權的使用者型別 {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-a472da6c57c74a94a179dda081004888}

**輸入(setCompanySettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控制代碼。 |
| overwriteMode | `xsd:string` | 否 | 資產覆寫模式。 |
| retainPublishState | `xsd:boolean` | 否 | 設定為`true`可在資產重新上傳時保留發佈狀態。 |
| defaultSourceProfileHandle | `xsd:string` | 否 | 要做為預設來源色彩設定檔的IccProfile資產。 |
| defaultDisplayProfileHandle | `xsd:string` | 否 | 要做為預設顯示色彩設定檔的IccProfile資產。 |
| iptcExifMappingXsltHandle | `xsd:string` | 否 | 用於將IPTC和EXIF中繼資料對應到IPS中繼資料欄位的XSL資產。 |
| Xmappingxslthandle | `xsd:string` | 否 | 用於將XMP中繼資料對應至IPS中繼資料欄位的XSL資產。 |
| diskSpaceWarningMin | `xsd:int` | 否 | 傳送警告訊息之前可用的最小可用磁碟空間（以KB為單位）。 |
| emailTrashCleanupWarning | `xsd:boolean` | 否 | 設為`true`，每當從垃圾桶清空資產時，就會傳送通知給公司管理員。 |

**輸出(setCompanySettingsReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

此程式碼範例設定公司的設定。

**要求**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**回應**

無。
