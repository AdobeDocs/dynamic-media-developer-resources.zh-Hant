---
description: 傳回影像格式，例如PDF、EPS、SWF等。
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 18%

---

# getImageFormats{#getimageformats}

傳回影像格式，例如PDF、EPS、SWF等。

語法

## 授權的使用者類型 {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-eefa36a70b74498f8727ef61d98cfb63}

**輸入(getImageFormatsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 使用您要取得的影像格式的公司控制代碼。 |

**輸出(getImageFormatsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`imageFormatArray`*` | `types:ImageFormatArray` | 是 | 影像格式陣列。 |

## 範例 {#section-73881e12839b4904bf3299b0920bdd0c}

此程式碼範例會傳回指定公司的所有影像格式。

**請求**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**回答**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```
