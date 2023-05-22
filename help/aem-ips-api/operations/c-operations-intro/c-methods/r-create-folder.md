---
title: 建立資料夾
description: 建立檔案夾。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 19%

---

# [!DNL createFolder]{#createfolder}

建立檔案夾。

>[!NOTE]
>
>新資料夾從屬於「影像」資料夾，即使您指定 `/` 以指明公司的根。

語法

## 授權用戶類型 {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對父資料夾的讀/寫權限。

## 參數 {#section-c00d8d89cf114886a535056f2a1bf892}

**輸入(createFolder)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把柄 |
| 資料夾路徑 | `xsd:string` | 是 | 用於將資料夾和所有子資料夾檢索到葉級別的根資料夾。 如果排除，則使用公司根。 |

**輸出(createFolderParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| folderHandle | `xsd:string` | 是 | 新資料夾的句柄。 |

## 範例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

此示例代碼在公司的根部建立資料夾。 響應返回新建立的資料夾的句柄。

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
