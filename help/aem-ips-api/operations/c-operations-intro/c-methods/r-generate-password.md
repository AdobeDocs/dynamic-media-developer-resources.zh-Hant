---
description: 產生新密碼。
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 16%

---

# generatePassword{#generatepassword}

產生新密碼。

語法

## 授權的使用者型別 {#section-88f7dc11e5c74be281399d8f2e3c9555}

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
| 密碼 | `xsd:string` | 是 | 新密碼。 |

## 範例 {#section-f580fefdccec46fe95359e3aef0ed17f}

此程式碼範例會產生密碼。 這很不尋常，因為要求只是引數，沒有任何包含的元素或值。 IPS會傳回強式密碼。

**要求**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**回應**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```
