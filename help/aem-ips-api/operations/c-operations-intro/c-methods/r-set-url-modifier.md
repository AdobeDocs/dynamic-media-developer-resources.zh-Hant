---
description: 設定指定資產的「影像伺服」或「影像演算」通訊協定命令。 這些命令可修改資產的表示法，而不會破壞資產。
seo-description: 設定指定資產的「影像伺服」或「影像演算」通訊協定命令。 這些命令可修改資產的表示法，而不會破壞資產。
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModifier{#seturlmodifier}

設定指定資產的「影像伺服」或「影像演算」通訊協定命令。 這些命令可修改資產的表示法，而不會破壞資產。

對於「影像伺服」，參數中的 `urlModifier` 指令會發佈在「修飾詞目錄」欄位中，並在請求URL上指定的任何指令之前套用。 中的命 `urlPostApplyModifier` 令將發佈到目錄 `PostModifier` 欄位，並會覆寫請求URL或中的任何命令 `urlModifier`。 在「影像演算」中，和中的 `urlModifier` 指令會串 `urlPostApplyModifier` 連並發佈至「修飾詞目錄」欄位。

## 授權使用者類型 {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**輸入(setUrlModifierParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| ` *`urlModifier`*` | `xsd:string` | 否 | 「影像伺服」或「影像演算」通訊協定指令，以在要求或指令之前套 `urlPostApplyModifier` 用。 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | 否 | 影像伺服或影像演算通訊協定指令，以套用在命令 `urlModifier` 和要求命令後。 |

**輸出(setUrlModifierReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-801d4b9b986443f59a5783a3d6bf44aa}

**請求**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**回答**

無。
