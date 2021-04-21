---
description: 重新命名資產。
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---


# renameAsset{#renameasset}

重新命名資產。

>[!NOTE]
>
>`renameFiles`參數已在舊版中過時，並已從`renameAsset`移除。 虛擬檔案路徑會變更為符合新資產名稱（保留副檔名），而物理檔案路徑則不受影響。 API用戶端在更新至新API版本時，必須移除此參數的參考。

## 授權用戶類型{#section-cc27ad713c6d498b8f056850b20976f4}

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
| `*`validateName`*` | `xsd:boolean` | 是 | 如果`validateName`是`true`，且資產類型需要唯一的IPS ID，則會檢查新名稱是否具有全局唯一性，如果`renameAsset`不是唯一的，則會引發故障。 |

**輸出(renameAssetReturn)**

IPS API不會傳回此作業的回應。 有關此元素的注意事項，請參閱`<ns1:validateName>`元素的說明。

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
