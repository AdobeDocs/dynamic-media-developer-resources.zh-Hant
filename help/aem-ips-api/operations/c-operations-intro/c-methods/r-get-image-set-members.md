---
description: 獲取映像集中的成員陣列。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 17%

---

# getImageSetMembers{#getimagesetmembers}

獲取映像集中的成員陣列。

語法

## 授權用戶類型 {#section-eaa3a167fa77403ea1b374b05fff4ded}

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

**Input(getImageSetMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 包含映像集的公司的句柄。 |
| 資產句柄 | `xsd:string` | 是 | 影像集資產句柄。 |

**輸出(getImageSetMembersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成員陣列 | `types:ImageSetMemberArray` | 否 | 影像整合員的陣列。 |

## 範例 {#section-888a9a78033346f39b171229de93dfa0}

此代碼示例返回特定映像整合員。 響應返回空陣列。

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
