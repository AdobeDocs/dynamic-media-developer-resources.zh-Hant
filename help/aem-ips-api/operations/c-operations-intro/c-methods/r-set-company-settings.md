---
description: 設定各種公司特定的組態值。
seo-description: 設定各種公司特定的組態值。
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
topic: Scene7 Image Production System API
uuid: 5908082f-6743-4444-ba73-757ad4664890
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setCompanySettings{#setcompanysettings}

設定各種公司特定的組態值。

語法

## 授權使用者類型 {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-a472da6c57c74a94a179dda081004888}

**輸入(setCompanySettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| ` *`overwriteMode`*` | `xsd:string` | 否 | 資產覆寫模式。 |
| ` *`retainPublishState`*` | `xsd:boolean` | 否 | 設定為 `true` 在資產重新上傳時保留發佈狀態。 |
| ` *`defaultSourceProfileHandle`*` | `xsd:string` | 否 | IccProfile資產，用作預設來源色彩描述檔。 |
| ` *`defaultDisplayProfileHandle`*` | `xsd:string` | 否 | IccProfile資產，用作預設顯示色彩描述檔。 |
| ` *`iptcExifMappingXsltHandle`*` | `xsd:string` | 否 | 用於將IPTC和EXIF中繼資料對應至IPS中繼資料欄位的XSL資產。 |
| ` *`xmpMappingXsltHandle`*` | `xsd:string` | 否 | 用於將XMP中繼資料對應至IPS中繼資料欄位的XSL資產。 |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | 否 | 在發送警告消息之前，可用的最小可用磁碟空間(KB)。 |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | 否 | 設定為在 `true` 資產從垃圾筒清空時，向公司管理員傳送通知。 |

**輸出(setCompanySettingsReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

此程式碼範例會設定公司的組態。

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
