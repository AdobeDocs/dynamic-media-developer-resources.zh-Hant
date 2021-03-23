---
description: 傳回影像格式，例如PDF、EPS、SWF等。
seo-description: 傳回影像格式，例如PDF、EPS、SWF等。
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 16%

---


# getImageFormats{#getimageformats}

傳回影像格式，例如PDF、EPS、SWF等。

語法

## 授權用戶類型{#section-6a386ad8641b4aa1a281600fc94fd3f6}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要取得之影像格式的公司控制代碼。 |

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

