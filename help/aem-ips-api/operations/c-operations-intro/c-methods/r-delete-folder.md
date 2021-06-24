---
description: 刪除資料夾。
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 10%

---

# deleteFolder{#deletefolder}

刪除資料夾。

語法

## 授權的使用者類型 {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對資料夾及其所有子資料夾的讀取和刪除訪問權限。

## 參數 {#section-a793c98a481a4f26ab50bc69b16b57e7}

**輸入(deleteFolderParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 資料夾所屬公司的句柄。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 要刪除的資料夾的句柄。 |

**輸出(deleteFolderParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-9d4617b322e8442d80e59be0f8714841}

此范常式式碼會從公司的根目錄中刪除資料夾。 它需要資料夾句柄，您必須從其他操作中獲取該句柄。

**請求**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

無。
