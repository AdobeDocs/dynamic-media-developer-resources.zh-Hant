---
description: 生成新密碼。
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 18%

---

# generatePassword{#generatepassword}

生成新密碼。

語法

## 授權的使用者類型 {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-d516615c906240819a284786efb19863}

**輸入(generatePasswordParam)**

無。

**輸出(generatePasswordParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`密碼`*` | `xsd:string` | 是 | 新密碼。 |

## 範例 {#section-f580fefdccec46fe95359e3aef0ed17f}

此程式碼範例會產生密碼。 這很不尋常，因為要求只是沒有任何封閉元素或值的參數。 IPS返回強密碼。

**請求**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**回答**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```
