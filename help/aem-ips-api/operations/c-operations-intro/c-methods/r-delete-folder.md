---
description: 刪除資料夾。
seo-description: 刪除資料夾。
seo-title: deleteFolder
solution: Experience Manager
title: deleteFolder
topic: Scene7 Image Production System API
uuid: 76af65fb-86ef-43e2-bfec-3682acf0afe6
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# deleteFolder{#deletefolder}

刪除資料夾。

語法

## 授權用戶類型{#section-1c15a74c41194744a81f5ca86fe26585}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 資料夾所屬公司的控制代碼。 |
| ` *`folderHandle`*` | `xsd:string` | 是 | 要刪除的資料夾的句柄。 |

**輸出(deleteFolderParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-9d4617b322e8442d80e59be0f8714841}

此范常式式碼會從公司根目錄中刪除資料夾。 它需要一個資料夾句柄，您必須從其他操作中獲取該句柄。

**請求**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

無。
