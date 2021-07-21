---
description: 獲取影像集中的成員陣列。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic, SDK/API，影像集
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 15%

---

# getImageSetMembers{#getimagesetmembers}

獲取影像集中的成員陣列。

語法

## 授權的使用者類型 {#section-eaa3a167fa77403ea1b374b05fff4ded}

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
>需要對映像和成員集資產的讀取訪問。

## 參數 {#section-a67ba98095574533980997c83ceaa316}

**輸入(getImageSetMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含影像集之公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 影像集資產控制代碼。 |

**輸出(getImageSetMembersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`memberArray`*` | `types:ImageSetMemberArray` | 否 | 影像整合員陣列。 |

## 範例 {#section-888a9a78033346f39b171229de93dfa0}

此程式碼範例會傳回特定影像整合員。 回應會傳回空白陣列。

**請求**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**回答**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```
