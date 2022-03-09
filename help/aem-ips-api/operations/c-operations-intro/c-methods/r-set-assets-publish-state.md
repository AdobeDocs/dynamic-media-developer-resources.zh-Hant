---
description: 確定是否準備發佈一批資產。
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 12%

---

# setAssetsPublishState{#setassetspublishstate}

確定是否準備發佈一批資產。

這是的批版本 [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563)。

## 授權用戶類型 {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對資產的讀寫權限。

## 參數 {#section-3e49d7859f8647b990d75373cc8dbc24}

**輸入(setAssetsPublishStateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | 是 | 資產的發佈狀態值的陣列。 |

**輸出(setAssetsPublishStateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成功計數 | `xsd:int` | 是 | 成功更新的資產數。 |
| 警告計數 | `xsd:int` | 是 | 操作嘗試更新時生成警告的資產數。 |
| 錯誤計數 | `xsd:int` | 是 | 操作嘗試刪除錯誤時生成錯誤的資產數。 |
| 警告DetailArray | `types:AssetOperationFaultArray` | 否 | 與生成警告的資產更新關聯的詳細資訊。 |
| 錯誤DetailArray | `types:AssetOperationFaultArray` | 否 | 與生成錯誤的資產更新關聯的詳細資訊。 |

## 範例 {#section-38cfdd3436214a06a1bae16875501d51}

此代碼示例設定資產的發佈狀態。

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
