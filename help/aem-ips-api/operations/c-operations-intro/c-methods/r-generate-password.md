---
description: 生成新密碼。
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

---


# generatePassword{#generatepassword}

生成新密碼。

語法

## 授權用戶類型{#section-88f7dc11e5c74be281399d8f2e3c9555}

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

此程式碼範例會產生密碼。 這很不尋常，因為請求只是不含任何封閉元素或值的參數。 IPS返回強口令。

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

