---
description: 設定與資產影像關聯的縮放目標。 它覆蓋現有縮放目標。
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 14%

---

# setZoomTargets{#setzoomtargets}

設定與資產影像關聯的縮放目標。 它覆蓋現有縮放目標。

語法

## 授權用戶類型 {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-161f8c733cc4439f94a06e12119d4226}

**Input(setZoomTargetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| 資產句柄 | `xsd:string` | 是 | 具有要設定的縮放目標的資產。 |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | 是 | 縮放目標定義的陣列。 |

**輸出(setZoomTargetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | 是 | 此操作建立的縮放目標的控制滑塊集。 |

## 範例 {#section-a2f14c7a1499443e96d099ea8a76c182}

此代碼示例按名稱、位置（x和y軸）、寬度、高度定義縮放目標的陣列，並將該陣列分配給資產。 響應包含對新建立的縮放目標的句柄。

**請求**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**回答**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```
