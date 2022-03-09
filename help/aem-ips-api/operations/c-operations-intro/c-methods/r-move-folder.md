---
description: 將資料夾移動到新位置。
solution: Experience Manager
title: 移動資料夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 28%

---

# 移動資料夾{#movefolder}

將資料夾移動到新位置。

語法

## 授權用戶類型 {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-473c2e68bcc14a9ea2593bee26e679dd}

**輸入(moveFolderParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 把手交給公司。 |
| folderHandle | `xsd:string` | 是 | 資料夾句柄。 |
| destFolderHandle | `xsd:string` | 是 | 目標資料夾的句柄。 |

**輸出(moveFolderReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| folderHandle | `xsd:string` | 是 | 已移動資料夾的句柄。 |

## 範例 {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**請求**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**回答**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```
