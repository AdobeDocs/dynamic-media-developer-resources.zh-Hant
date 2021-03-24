---
description: 獲取映像集中的成員陣列。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media經典，SDK/API，影像集
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 15%

---


# getImageSetMembers{#getimagesetmembers}

獲取映像集中的成員陣列。

語法

## 授權用戶類型{#section-eaa3a167fa77403ea1b374b05fff4ded}

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
>需要對映像和成員集資產的讀取訪問權。

## 參數 {#section-a67ba98095574533980997c83ceaa316}

**輸入(getImageSetMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含影像集之公司的控點。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 影像設定資產控制代碼。 |

**輸出(getImageSetMembersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`memberArray`*` | `types:ImageSetMemberArray` | 否 | 映像整合員的陣列。 |

## 範例 {#section-888a9a78033346f39b171229de93dfa0}

此程式碼範例會傳回特定的影像整合員。 響應返回空陣列。

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

