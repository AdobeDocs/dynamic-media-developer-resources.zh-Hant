---
description: 建立衍生自現有主影像資產的新資產。
seo-description: 建立衍生自現有主影像資產的新資產。
seo-title: createDerivedAsset
solution: Experience Manager
title: createDerivedAsset
topic: Scene7 Image Production System API
uuid: e1f9b690-af34-4da5-a534-c3a8c6b0a8fc
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# createDerivedAsset{#createderivedasset}

建立衍生自現有主影像資產的新資產。

語法

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

衍生資產會指定影像伺服器通訊協定命令，以修改擁有者影像的表示法。 衍 `AdjustedView` 生類型有助於對單一影像套用簡單修改（例如，指定裁切矩形），而 `LayerView` 則有助於建立可包含文字或其他影像的多圖層檢視。

與影像復本(請參 [閱copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0))不同，衍生影像會連結至其擁有者影像。 對擁有者影像的變更會修改相關的衍生資產。 刪除擁有者影像將會刪除任何相關的衍生影像。

## 授權使用者類型 {#authorized-user-types}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 包含您將從中衍生新資產之資產的公司控制代碼。 |
| ` *`ownerHandle`*` | `xsd:string` | 是 | 新影像衍生自的主影像資產控制代碼。 |
| ` *`folderHandle`*` | `xsd:string` | 是 | 將在其中建立新派生資產的資料夾的句柄。 |
| ` *`名稱`*` | `xsd:string` | 是 | 衍生資產的名稱。 |
| ` *`類型`*` | `xsd:string` | 是 | 新衍生資產的資產類型：或 `AdjustedView` 者 `LayerView`。 |
| ` *`urlModifier`*` | `xsd:string` | 否 | 在請求或命令之前應用影像 *服務* 或影像渲染協 `urlPostApplyModifier` 議命令。 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | 否 | 在請求或命令之後套用影像 *伺服* 或影像轉換通 `urlPostApplyModifier` 訊協定命令。 |

**輸出(createDerivedAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | 是 | 衍生資產的控制代碼。 |

## 範例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

范常式式碼會建立具有調整檢視和任意值 `urlModifier` 的 `urlPostApplyModifier` 衍生資產。 回應會將控制代碼傳回新衍生的資產。

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

