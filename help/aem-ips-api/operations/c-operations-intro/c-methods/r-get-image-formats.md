---
description: 返回影像格式，如PDF、EPS、SWF等。
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 20%

---

# getImageFormats{#getimageformats}

返回影像格式，如PDF、EPS、SWF等。

語法

## 授權用戶類型 {#section-6a386ad8641b4aa1a281600fc94fd3f6}

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
| 公司句柄 | `xsd:string` | 是 | 要獲取的影像格式的公司句柄。 |

**輸出(getImageFormatsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | 是 | 影像格式陣列。 |

## 範例 {#section-73881e12839b4904bf3299b0920bdd0c}

此代碼示例返回指定公司的所有影像格式。

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
