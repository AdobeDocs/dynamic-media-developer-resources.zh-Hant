---
description: 從公司刪除專案。 資產和專案之間的連結會中斷，但不會從IPS中刪除資產。
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---

# deleteProject{#deleteproject}

從公司刪除專案。 資產和專案之間的連結會中斷，但不會從IPS中刪除資產。

語法

## 授權的使用者類型 {#section-d8a70e23c68d426e9af1357b978ae2f0}

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
| `*`companyName`*` | `xsd:string` | 是 | 與項目關聯的公司名稱。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 要刪除的項目的句柄。 |

**輸出(deleteProjectReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-e38507f1f7ec41b9a625f47390490254}

此代碼示例使用公司句柄和項目句柄作為發送到IPS Web服務伺服器的deleteProjectParam中的欄位，以刪除項目。

**請求**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**回答**

無。
