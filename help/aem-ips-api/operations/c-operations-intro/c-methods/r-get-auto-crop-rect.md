---
description: 根據影像的背景顏色或透明度返回影像的裁剪區域。
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 15%

---

# getAutoCropRect{#getautocroprect}

根據影像的背景顏色或透明度返回影像的裁剪區域。

語法

## 授權用戶類型 {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**輸入(getAutoCropRectParam)**

>[!NOTE]
>
>在調用此方法時指定autoColorCropOptions或autoTransparentCropOptions。

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 要使用資產的公司的句柄。 |
| 資產句柄 | `xsd:string` | 是 | 要使用的資產的句柄。 |
| 自動顏色裁剪選項 | `types:AutoColorCropOptions` | 否 | 根據顏色計算裁剪矩形。 請參閱 [自動顏色裁剪選項](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)。 |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | 否 | 根據透明度計算裁剪矩形。 請參閱 [自動透明裁剪選項](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)。 |

**輸出(getAutoCropRectReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| x偏移 | `xsd:int` | 是 | 計算裁剪區域的起始左像素坐標。 |
| y偏移 | `xsd:int` | 是 | 計算的裁剪區域的起始頂像素坐標。 |
| 寬度 | `xsd:int` | 是 | 計算的裁剪區域的寬度（以像素為單位）。 |
| 高度 | `xsd:int` | 是 | 計算的裁剪區域的高度（以像素為單位）。 |

## 範例 {#section-ba65bd66086d491cad1cea535954ee1f}

**請求**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**回答**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [自動顏色裁剪選項](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [自動透明裁剪選項](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

