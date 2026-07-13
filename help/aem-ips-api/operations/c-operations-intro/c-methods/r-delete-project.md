---
description: 從公司刪除專案。 資產和專案之間的連結已中斷，但資產不會從IPS刪除。
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
TQID: 'https://experienceleague.adobe.com/gZaX8EqLg3A4ca6EY9-xsFkz4HzWFbmLU2xsgU-LM-M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 7%

---

# deleteProject{#deleteproject}

從公司刪除專案。 資產和專案之間的連結已中斷，但資產不會從IPS刪除。

語法

## 授權的使用者型別 {#section-d8a70e23c68d426e9af1357b978ae2f0}

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
| companyName | `xsd:string` | 是 | 與專案相關聯之公司的名稱。 |
| projectHandle | `xsd:string` | 是 | 要刪除的專案的控制代碼。 |

**輸出(deleteProjectReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-e38507f1f7ec41b9a625f47390490254}

此程式碼範例使用公司控制代碼和專案控制代碼作為傳送至IPS Web服務伺服器以刪除專案之deleteProjectParam中的欄位。

**要求**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**回應**

無。

