---
description: 傳回特定公司的IPS設定。
solution: Experience Manager
title: getcompanysettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b9f41405-8a45-416c-acec-ef22c2ee119e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 25%

---

# getcompanysettings{#getcompanysettings}

傳回特定公司的IPS設定。

語法

## 授權的使用者型別 {#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e146f479c2744baa8f68be8c8848c97f}

**輸入(getCompanySettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 您要擷取其設定的公司的控制代碼。 |

**輸出(getCompanySettingsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 設定 | `types:CompanySettings` | 是 | 公司設定。 |

## 範例 {#section-191f78995ecf473a95eadf7296204fd7}

此程式碼範例會傳回特定公司的所有IPS設定。

**請求**

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**回答**

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```
