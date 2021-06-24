---
description: 建立檔案夾。
solution: Experience Manager
title: 建立資料夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 18%

---

# [!DNL createFolder]{#createfolder}

建立檔案夾。

>[!NOTE]
>
>即使您指定`/`來指出公司的根，新資料夾仍隸屬於「影像」資料夾。

語法

## 授權的使用者類型 {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對父資料夾的讀/寫訪問權限。

## 參數 {#section-c00d8d89cf114886a535056f2a1bf892}

**輸入(createFolder)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 對公司的控制 |
| `*`folderPath`*` | `xsd:string` | 是 | 用於檢索資料夾和所有子資料夾到葉級別的根資料夾。 如果排除，則會使用公司根。 |

**輸出(createFolderParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 是 | 新資料夾的處理。 |

## 範例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

此范常式式碼會在公司的根目錄中建立資料夾。 回應會傳回新建立資料夾的控制代碼。

**請求**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**回答**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
