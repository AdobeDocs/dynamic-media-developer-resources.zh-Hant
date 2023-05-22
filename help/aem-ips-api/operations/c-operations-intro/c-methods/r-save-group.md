---
description: 建立或編輯組。
solution: Experience Manager
title: 保存組
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 22%

---

# 保存組{#savegroup}

建立或編輯組。

語法

## 授權用戶類型 {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-743610e98dd5494baffcbad6401038eb}

**輸入(saveGroupParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 要保存的組所在公司的句柄。 |
| 組句柄 | `xsd:string` | 否 | 組的句柄。 |
| name | `xsd:string` | 是 | 群組名稱. |
| isSystemDefined | `xsd:boolean` | 是 | `false` 為預設值。 |

**輸出(saveGroupReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 組句柄 | `xsd:string` | 是 | 組句柄。 |

## 範例 {#section-26eee227ff1f4edabb7fa1240b4d9999}

此代碼示例建立屬於特定公司的組。 如果組已存在，則會使用您指定的參數值保存該組。

**請求**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**回答**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```
