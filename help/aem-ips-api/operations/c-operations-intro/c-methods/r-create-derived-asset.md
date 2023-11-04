---
description: 建立衍生自現有主要來源影像資產的新資產。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

建立衍生自現有主要來源影像資產的新資產。

語法

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

衍生資產會指定影像伺服器通訊協定命令，以修改擁有者影像的表示方式。 此 `AdjustedView` 衍生型別有助於將簡單的修改套用至單一影像（例如，藉由指定裁切矩形），而 `LayerView` 協助建立可能包含文字或其他影像的多層檢視。

與影像復本不同(請參閱 [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0))，則衍生影像會連結至其擁有者影像。 所有者影像的變更會修改關聯的衍生資產。 刪除擁有者影像會刪除任何關聯的衍生影像。

## 授權的使用者型別 {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-5a0dde01cff6454da3646ea805c2be1e}

**輸入(createDerivedAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含新資產之資產的公司的控制代碼。 |
| ownerHandle | `xsd:string` | 是 | 衍生新影像的主要影像資產的控點。 |
| folderHandle | `xsd:string` | 是 | 建立新衍生資產的資料夾的控制代碼。 |
| name | `xsd:string` | 是 | 衍生資產的名稱。 |
| type | `xsd:string` | 是 | 新衍生資產的資產型別： `AdjustedView` 或 `LayerView`. |
| urlModifier | `xsd:string` | 否 | 影像伺服或影像演算通訊協定命令已套用 *早於* 要求或 `urlPostApplyModifier` 命令。 |
| urlPostApplyModifier | `xsd:string` | 否 | 影像伺服或影像演算通訊協定命令已套用 *晚於* 至請求或 `urlPostApplyModifier` 命令。 |

**輸出(createDerivedAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 衍生資產的控點。 |

## 範例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

範常式式碼會建立衍生資產，並包含調整後的檢視和 `urlModifier` 和 `urlPostApplyModifier` 具有任意值。 回應會將控制代碼傳回至新衍生的資產。

**請求**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**回答**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```
