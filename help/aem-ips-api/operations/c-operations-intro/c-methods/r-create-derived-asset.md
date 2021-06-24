---
description: 建立衍生自現有主要來源影像資產的新資產。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

建立衍生自現有主要來源影像資產的新資產。

語法

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生資產指定用於修改所有者映像的表示的映像伺服器協定命令。 `AdjustedView`衍生類型有助於對單一影像應用簡單修改（例如，通過指定裁切矩形），而`LayerView`有助於建立可包含文本或其他影像的多層視圖。

與影像副本（請參閱[copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)）不同，衍生影像連結至其擁有者影像。 對擁有者影像的變更會修改相關的衍生資產。 刪除擁有者影像將刪除任何相關的衍生影像。

## 授權的使用者類型 {#authorized-user-types}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您將從中衍生新資產之資產的公司控制代碼。 |
| `*`ownerHandle`*` | `xsd:string` | 是 | 衍生新影像的主要影像資產的控制代碼。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 將在其中建立新派生資產的資料夾的句柄。 |
| `*`名稱`*` | `xsd:string` | 是 | 衍生資產的名稱。 |
| `*`類型`*` | `xsd:string` | 是 | 新衍生資產的資產類型：`AdjustedView`或`LayerView`。 |
| `*`urlModifier`*` | `xsd:string` | 否 | 在&#x200B;*請求或`urlPostApplyModifier`命令之前應用*&#x200B;的影像服務或影像呈現協定命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 否 | 在&#x200B;*之後*&#x200B;應用到請求或`urlPostApplyModifier`命令的影像伺服或影像呈現協定命令。 |

**輸出(createDerivedAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 衍生資產的控制代碼。 |

## 範例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

范常式式碼會建立衍生資產，其中包含調整後的檢視，以及具有任意值的`urlModifier`和`urlPostApplyModifier`。 回應會將控制代碼傳回至新衍生的資產。

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
