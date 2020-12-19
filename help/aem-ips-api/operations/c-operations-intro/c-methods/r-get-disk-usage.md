---
description: 傳回有關公司結構（檔案數等）的資訊。
seo-description: 傳回有關公司結構（檔案數等）的資訊。
seo-title: getDiskUsage
solution: Experience Manager
title: getDiskUsage
topic: Scene7 Image Production System API
uuid: 29190200-8f49-4689-9782-1df665dca1b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 12%

---


# getDiskUsage{#getdiskusage}

傳回有關公司結構（檔案數等）的資訊。

## 授權用戶類型{#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**輸入(getDiskUsageParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 您要取得其磁碟使用情形之公司的控制代碼。 |

**輸出(getDiskUsageReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`diskUsageArray`*` | `types:DiskUsageArray` | 是 | 公司磁碟的使用陣列。 |

## 範例 {#section-cb16a97badc94076ad5da277db5ed16a}

此請求的名稱具有誤導性。 它不僅僅返回反映公司使用多少磁碟空間的標量值，還獲取了有關公司結構的其他資訊。

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

