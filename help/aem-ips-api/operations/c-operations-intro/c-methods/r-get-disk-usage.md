---
description: 傳回公司結構（檔案數等）的相關資訊。
solution: Experience Manager
title: getdiskusage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
TQID: 'https://experienceleague.adobe.com/mF0YHIw8BZhBRK240EmiiaHoyBbTdaW-ajl7veY1ywk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 11%

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

**要求**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**回應**

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

