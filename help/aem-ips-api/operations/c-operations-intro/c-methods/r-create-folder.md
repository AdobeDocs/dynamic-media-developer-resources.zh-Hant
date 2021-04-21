---
description: 建立檔案夾。
solution: Experience Manager
title: 建立資料夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 18%

---


# [!DNL createFolder]{#createfolder}

建立檔案夾。

>[!NOTE]
>
>新資料夾隸屬於「影像」資料夾，即使您指定`/`來指出公司的根目錄亦然。

語法

## 授權用戶類型{#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對父資料夾的讀／寫訪問權限。

## 參數 {#section-c00d8d89cf114886a535056f2a1bf892}

**輸入(createFolder)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手 |
| `*`folderPath`*` | `xsd:string` | 是 | 用於將資料夾和所有子資料夾檢索到葉層的根資料夾。 如果排除，則會使用公司根目錄。 |

**輸出(createFolderParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 是 | 新資料夾的句柄。 |

## 範例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

此范常式式碼會在公司根目錄下建立資料夾。 響應返回新建資料夾的句柄。

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

