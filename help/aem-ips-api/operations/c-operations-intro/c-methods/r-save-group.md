---
description: 建立或編輯群組。
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 20%

---

# saveGroup{#savegroup}

建立或編輯群組。

語法

## 授權的使用者類型 {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-743610e98dd5494baffcbad6401038eb}

**輸入(saveGroupParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 含有您要儲存之群組的公司控制代碼。 |
| `*`groupHandle`*` | `xsd:string` | 否 | 組的句柄。 |
| `*`名稱`*` | `xsd:string` | 是 | 群組名稱. |
| `*`isSystemDefined`*` | `xsd:boolean` | 是 | `false` 為預設值。 |

**輸出(saveGroupReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | 是 | 組句柄。 |

## 範例 {#section-26eee227ff1f4edabb7fa1240b4d9999}

此程式碼範例會建立屬於特定公司的群組。 如果組已存在，則會使用您指定的參數值保存該組。

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
