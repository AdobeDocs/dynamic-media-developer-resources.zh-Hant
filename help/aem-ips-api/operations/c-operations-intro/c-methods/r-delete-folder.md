---
description: 刪除資料夾。
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
TQID: 'https://experienceleague.adobe.com/OfZbcMyLmLvg6x088Y5y0DBM7-C--jW7oPtOfIaSwDk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 10%

---

# deleteFolder{#deletefolder}

刪除資料夾。

語法

## 授權的使用者型別 {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資料夾及其所有子項的讀取和刪除存取權。

## 參數 {#section-a793c98a481a4f26ab50bc69b16b57e7}

**輸入(deleteFolderParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 資料夾所屬公司的控制代碼。 |
| folderHandle | `xsd:string` | 是 | 要刪除的資料夾的控制代碼。 |

**輸出(deleteFolderParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-9d4617b322e8442d80e59be0f8714841}

此程式碼範例會從公司的根目錄中刪除資料夾。 它需要資料夾控制代碼，您必須從其他作業取得此控制代碼。

**要求**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

無。
