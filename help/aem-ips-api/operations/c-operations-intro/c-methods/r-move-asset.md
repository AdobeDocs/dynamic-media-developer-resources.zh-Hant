---
description: 將資產移動到特定資料夾。
solution: Experience Manager
title: 移動資產
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 17%

---

# 移動資產{#moveasset}

將資產移動到特定資料夾。

語法

## 授權用戶類型 {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-dd0bbdf293aa4563af70a91f97c861f1}

**輸入(moveAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 把手交給公司。 |
| 資產句柄 | `xsd:string` | 是 | 處理要移動的資產。 |
| folderHandle | `xsd:string` | 是 | 目標資料夾的句柄。 |

**輸出(moveAssetReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-78333769f4f14e2886fdf06433c9d2ad}

此代碼示例將資產移到資料夾。

**請求**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**回答**

無。
