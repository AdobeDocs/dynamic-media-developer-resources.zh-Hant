---
description: 傳回公司結構（檔案數等）的相關資訊。
solution: Experience Manager
title: getdiskusage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 13%

---

# getdiskusage{#getdiskusage}

傳回公司結構（檔案數等）的相關資訊。

## 授權的使用者型別 {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**輸入(getDiskUsageParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 您要取得其磁碟使用量的公司的控制代碼。 |

**輸出(getDiskUsageReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| diskUsageArray | `types:DiskUsageArray` | 是 | 公司磁碟使用的陣列。 |

## 範例 {#section-cb16a97badc94076ad5da277db5ed16a}

此請求的名稱會誤導人。 它不會只傳回反映公司使用磁碟空間的純量值，而是會取得有關公司結構的其他資訊。

**請求**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**回答**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```
