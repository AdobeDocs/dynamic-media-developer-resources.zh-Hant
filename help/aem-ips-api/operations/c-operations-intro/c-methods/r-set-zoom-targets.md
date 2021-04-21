---
description: 設定與資產影像相關聯的縮放目標。 它會覆寫現有的縮放目標。
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 13%

---


# setZoomTargets{#setzoomtargets}

設定與資產影像相關聯的縮放目標。 它會覆寫現有的縮放目標。

語法

## 已授權的使用者類型{#section-c5e1863e9cb1426591bfea513620b6ab}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 包含您要設定之縮放目標的資產。 |
| `*`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | 是 | 縮放目標定義的陣列。 |

**輸出(setZoomTargetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`zoomTargetHandleArray`*` | `types:HandleArray` | 是 | 此操作建立的縮放目標的控點集。 |

## 範例 {#section-a2f14c7a1499443e96d099ea8a76c182}

此程式碼範例依名稱、位置（x和y軸）、寬度、高度定義縮放目標的陣列，並將陣列指派給資產。 回應包含新建立之縮放目標的控點。

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

