---
description: 刪除資料夾。
solution: Experience Manager
title: 刪除資料夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 11%

---

# 刪除資料夾{#deletefolder}

刪除資料夾。

語法

## 授權用戶類型 {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對資料夾及其所有子資料夾的讀取和刪除權限。

## 參數 {#section-a793c98a481a4f26ab50bc69b16b57e7}

**輸入(deleteFolderParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 資料夾所屬公司的句柄。 |
| folderHandle | `xsd:string` | 是 | 要刪除的資料夾的句柄。 |

**輸出(deleteFolderParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-9d4617b322e8442d80e59be0f8714841}

此示例代碼從公司根目錄中刪除一個資料夾。 它需要一個資料夾句柄，您必須從其他操作中獲取該句柄。

**請求**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

無。
