---
description: 取得影像集中的成員陣列。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
TQID: 'https://experienceleague.adobe.com/7tS3wEIqaBPmykuVmDBfq9GugDcbnevj-XAQQHM3icY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 14%

---

# getImageSetMembers{#getimagesetmembers}

取得影像集中的成員陣列。

語法

## 授權的使用者型別 {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>需要影像和成員集資產的讀取存取權。

## 參數 {#section-a67ba98095574533980997c83ceaa316}

**輸入(getImageSetMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含影像集之公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 影像集資產控制代碼。 |

**輸出(getImageSetMembersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | 否 | 影像整合員的陣列。 |

## 範例 {#section-888a9a78033346f39b171229de93dfa0}

此程式碼範例會傳回特定的影像整合員。 回應會傳回空白陣列。

**要求**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**回應**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```
