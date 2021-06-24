---
description: 傳回標示為要發佈的資產的發佈內容。
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 15%

---

# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

傳回標示為要發佈的資產的發佈內容。

語法

## 授權的使用者類型 {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>* 使用者必須具有讀取存取權，才能傳回資產。
>* 所有使用者都可存取共用公司。

>



## 參數 {#section-1742fcb196224545b270eb8241f757a8}

**輸入(batchGetAssetPublishContextsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司處理。 |
| `*`assetHandleArray`*` | ` `類型：HandleArray&quot; | 是 | 您要查詢作用中（針對發佈而標示）內容的資產清單。 |

**輸出(batchGetAssetPublishContextsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetPublishContextsArray`*` | `types:assetPublishContextsArray` | 是 | 發佈內容的陣列，其中每個資產都會標示為要發佈。 |

## 範例 {#section-457f6809ccfa425b9a0976313d613f4e}

**請求**

```java
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**回答**

```java
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```
