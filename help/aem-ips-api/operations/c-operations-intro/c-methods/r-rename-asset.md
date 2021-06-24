---
description: 重新命名資產。
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# renameAsset{#renameasset}

重新命名資產。

>[!NOTE]
>
>先前版本已棄用`renameFiles`參數，並從`renameAsset`中移除。 虛擬檔案路徑會變更，以符合新資產名稱（保留副檔名），而物理檔案路徑則不受影響。 更新至新API版本時，API用戶端需要移除此參數的參考。

## 授權的使用者類型 {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和寫入存取權。

## 參數 {#section-ef95a994106841e0ab346dd4cf672258}

**輸入(renameAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 資產所屬公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 您要重新命名的資產的控制代碼。 |
| `*`newName`*` | `xsd:string` | 是 | 資產的新名稱。 |
| `*`validateName`*` | `xsd:boolean` | 是 | 如果`validateName`為`true`，且資產類型需要唯一IPS ID，則會檢查新名稱是否具有全域唯一性，而如果`renameAsset`並非唯一，則會擲回錯誤。 |

**輸出(renameAssetReturn)**

IPS API不會針對此操作傳回回應。 請參閱`<ns1:validateName>`元素的說明，了解此元素的警告。

## 範例 {#section-a0ddffd62bec42e09069f22ceb486f8a}

此程式碼範例會重新命名資產

**請求**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**回答**

無。
