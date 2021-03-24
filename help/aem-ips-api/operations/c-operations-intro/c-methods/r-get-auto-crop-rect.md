---
description: 根據影像的背景顏色或透明度傳回影像的裁切區域。
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 14%

---


# getAutoCropRect{#getautocroprect}

根據影像的背景顏色或透明度傳回影像的裁切區域。

語法

## 授權用戶類型{#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

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
>在呼叫此方法時，指定`*`autoColorCropOptions`*`或`*`autoTransparentCropOptions`*`。

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要使用之資產的公司控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 您要使用之資產的控制代碼。 |
| `*`autoColorCropOptions`*` | `types:AutoColorCropOptions` | 否 | 根據顏色計算裁切矩形。 請參閱[AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)。 |
| `*`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | 否 | 根據透明度計算裁切矩形。 請參閱[AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)。 |

**輸出(getAutoCropRectReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`xOffset`*` | `xsd:int` | 是 | 計算的裁切區域的左起像素坐標。 |
| `*`yOffset`*` | `xsd:int` | 是 | 計算的裁切區域的起始頂像素坐標。 |
| `*`width`*` | `xsd:int` | 是 | 計算的裁切區域的寬度（以像素為單位）。 |
| `*`height`*` | `xsd:int` | 是 | 計算的裁切區域的高度（以像素為單位）。 |

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
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

