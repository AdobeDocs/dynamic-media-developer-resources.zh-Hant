---
description: 建立或編輯縮放目標。
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 20%

---

# saveZoomTarget{#savezoomtarget}

建立或編輯縮放目標。

語法

## 授權用戶類型 {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-4a23983cae4e49a098e9bbe736933996}

**輸入(saveZoomTargetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 包含要保存的縮放目標的公司的句柄。 |
| 資產句柄 | `xsd:string` | 是 | 縮放目標的句柄。 |
| zoomTargetHandle | `xsd:string` | 否 | 編輯或建立縮放目標。 |
| name | `xsd:string` | 是 | 縮放目標名稱。 |
| x位置 | `xsd:int` | 是 | 左像素位置。 |
| 位置 | `xsd:int` | 是 | 頂像素位置。 |
| 寬度 | `xsd:int` | 是 | 縮放目標寬度。 |
| 高度 | `xsd:int` | 是 | 縮放目標高度。 |
| 用戶資料 | `xsd:string` | 是 | 有關特定於客戶的資訊。 可以包含任何類型的資料。 |

**輸出(saveZoomTargetReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| zoomTargetHandle | `xsd:string` | 是 | 對新建立的縮放目標的句柄。 |

## 範例 {#section-509c472c316549cdb228d7e1cfa8400a}

此代碼示例保存縮放目標。 響應返回縮放目標句柄。

**請求**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**回答**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```
