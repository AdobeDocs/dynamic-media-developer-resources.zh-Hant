---
title: 建立資料夾
description: 建立檔案夾。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
TQID: 'https://experienceleague.adobe.com/iQNFDdsbxhklGSfUb1pmcNhzIT8kJYc19xFglU7Blc8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 17%

---

# [!DNL createFolder]{#createfolder}

建立檔案夾。

>[!NOTE]
>
>新資料夾隸屬於Images資料夾，即使您指定了`/`來指示公司的根目錄亦然。

語法

## 授權的使用者型別 {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須具有上層資料夾的讀取/寫入存取權。

## 參數 {#section-c00d8d89cf114886a535056f2a1bf892}

**輸入(createFolder)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼 |
| 資料夾路徑 | `xsd:string` | 是 | 用來擷取葉層級資料夾及所有子資料夾的根資料夾。 如果排除，則會使用公司根目錄。 |

**輸出(createFolderParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| folderHandle | `xsd:string` | 是 | 新資料夾的控制代碼。 |

## 範例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

此範常式式碼會在公司的根目錄下建立資料夾。 回應會傳回新建立資料夾的控制代碼。

**要求**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**回應**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```

