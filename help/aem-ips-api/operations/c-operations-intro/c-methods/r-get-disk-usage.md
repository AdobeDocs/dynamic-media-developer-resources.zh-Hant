---
description: 傳回有關公司結構（檔案數等）的資訊。
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 13%

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
| `*`companyHandle`*` | `xsd:string` | 是 | 您要取得其磁碟使用情形之公司的控制代碼。 |

**輸出(getDiskUsageReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | 是 | 公司磁碟的使用陣列。 |

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

