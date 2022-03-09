---
description: 從公司中刪除項目。 資產和項目之間的連結已斷開，但資產不會從IPS中刪除。
solution: Experience Manager
title: 刪除項目
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 9%

---

# 刪除項目{#deleteproject}

從公司中刪除項目。 資產和項目之間的連結已斷開，但資產不會從IPS中刪除。

語法

## 授權用戶類型 {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-00d1e00dd5014513a52b4e6b4f61de62}

**輸入(deleteProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司名稱 | `xsd:string` | 是 | 與項目關聯的公司的名稱。 |
| 項目句柄 | `xsd:string` | 是 | 要刪除的項目的句柄。 |

**輸出(deleteProjectReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-e38507f1f7ec41b9a625f47390490254}

此代碼示例將公司句柄和項目句柄用作發送到IPS Web服務伺服器的deleteProjectParam中的欄位，以刪除項目。

**請求**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**回答**

無。
