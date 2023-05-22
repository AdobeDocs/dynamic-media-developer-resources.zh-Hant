---
description: 建立從現有主源映像資產派生的新資產。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

建立從現有主源映像資產派生的新資產。

語法

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生的資產指定修改所有者映像表示的映像伺服器協定命令。 的 `AdjustedView` 派生類型有助於對單個影像應用簡單修改（例如，通過指定裁剪矩形），而 `LayerView` 幫助建立可能包含文本或附加影像的多層視圖。

與影像副本不同(請參見 [複製映像](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0))，派生映像連結到其所有者映像。 對所有者映像的更改將修改關聯的派生資產。 刪除所有者映像將刪除任何關聯的派生映像。

## 授權用戶類型 {#authorized-user-types}

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
| 公司句柄 | `xsd:string` | 是 | 包含要從中獲取新資產的資產的公司的句柄。 |
| 所有者句柄 | `xsd:string` | 是 | 導出新映像的主映像資產的句柄。 |
| folderHandle | `xsd:string` | 是 | 建立新派生資產的資料夾的句柄。 |
| name | `xsd:string` | 是 | 派生資產的名稱。 |
| type | `xsd:string` | 是 | 新衍生資產的資產類型： `AdjustedView` 或 `LayerView`。 |
| url修飾符 | `xsd:string` | 否 | 應用了影像服務或影像呈現協定命令 *先* 請求或 `urlPostApplyModifier` 的雙曲餘切值。 |
| urlPostApplyModifier | `xsd:string` | 否 | 應用了影像服務或影像呈現協定命令 *後* 請求或 `urlPostApplyModifier` 的雙曲餘切值。 |

**輸出(createDerivedAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 資產句柄 | `xsd:string` | 是 | 派生資產的句柄。 |

## 範例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

示例代碼建立具有調整視圖和 `urlModifier` 和 `urlPostApplyModifier` 具有任意值。 響應將句柄返回到新派生的資產。

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
