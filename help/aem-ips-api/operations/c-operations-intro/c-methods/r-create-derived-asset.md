---
description: 建立衍生自現有主要來源影像資產的新資產。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 8%

---


# createDerivedAsset{#createderivedasset}

建立衍生自現有主要來源影像資產的新資產。

語法

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

衍生資產會指定影像伺服器通訊協定命令，以修改擁有者影像的表示法。 `AdjustedView`衍生類型有助於對單一影像套用簡單修改（例如，指定裁切矩形），而`LayerView`則有助於建立可包含文字或其他影像的多圖層檢視。

與影像復本（請參閱[copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)）不同，衍生影像會連結至其擁有者影像。 對擁有者影像的變更會修改相關的衍生資產。 刪除擁有者影像將會刪除任何相關的衍生影像。

## 授權用戶類型{#authorized-user-types}

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
| `*`ownerHandle`*` | `xsd:string` | 是 | 新影像將從中衍生的主要影像資產的控制代碼。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 將在其中建立新派生資產的資料夾的句柄。 |
| `*`名稱`*` | `xsd:string` | 是 | 衍生資產的名稱。 |
| `*`類型`*` | `xsd:string` | 是 | 新衍生資產的資產類型：`AdjustedView`或`LayerView`。 |
| `*`urlModifier`*` | `xsd:string` | 否 | 在&#x200B;*請求或`urlPostApplyModifier`命令之前應用*&#x200B;的影像服務或影像渲染協定命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 否 | 將&#x200B;*after*&#x200B;的影像伺服或影像轉換通訊協定指令套用至要求或`urlPostApplyModifier`指令。 |

**輸出(createDerivedAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 衍生資產的控制代碼。 |

## 範例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

范常式式碼會建立具有調整檢視的衍生資產，以及具有任意值的`urlModifier`和`urlPostApplyModifier`。 回應會將控制代碼傳回新衍生的資產。

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

