---
description: 建立或編輯縮放目標。
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 19%

---


# saveZoomTarget{#savezoomtarget}

建立或編輯縮放目標。

語法

## 授權用戶類型{#section-823cd9f0557045bca51da66768b5ba74}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要儲存之縮放目標之公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 縮放目標的控點。 |
| `*`zoomTargetHandle`*` | `xsd:string` | 否 | 編輯或建立縮放目標。 |
| `*`名稱`*` | `xsd:string` | 是 | 縮放目標名稱。 |
| `*`xPosition`*` | `xsd:int` | 是 | 左側像素位置。 |
| `*`yPosition`*` | `xsd:int` | 是 | 最上方像素位置。 |
| `*`width`*` | `xsd:int` | 是 | 縮放目標寬度。 |
| `*`height`*` | `xsd:int` | 是 | 縮放目標高度。 |
| `*`使用者資料`*` | `xsd:string` | 是 | 針對特定客戶的資訊。 可以包含任何類型的資料。 |

**輸出(saveZoomTargetReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | 是 | 控制代碼至新建立的縮放目標。 |

## 範例 {#section-509c472c316549cdb228d7e1cfa8400a}

此程式碼範例會儲存縮放目標。 回應會傳回縮放目標控制代碼。

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

