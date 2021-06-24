---
description: 判斷一批資產是否已準備好發佈。
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 12%

---

# setAssetsPublishState{#setassetspublishstate}

判斷一批資產是否已準備好發佈。

這是[setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563)的批版本。

## 授權的使用者類型 {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和寫入存取權。

## 參數 {#section-3e49d7859f8647b990d75373cc8dbc24}

**輸入(setAssetsPublishStateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | 是 | 資產的發佈狀態值陣列。 |

**輸出(setAssetsPublishStateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功更新資產的數量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作嘗試更新時產生警告的資產數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作嘗試刪除時產生錯誤的資產數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與產生警告的資產更新相關的詳細資料。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與產生錯誤的資產更新相關的詳細資料。 |

## 範例 {#section-38cfdd3436214a06a1bae16875501d51}

此程式碼範例會設定資產的發佈狀態。

**請求**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**回答**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```
