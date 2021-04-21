---
description: 設定指定資產的「影像伺服」或「影像演算」通訊協定命令。 這些命令可修改資產的表示法，而不會破壞資產。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 7%

---


# setUrlModifier{#seturlmodifier}

設定指定資產的「影像伺服」或「影像演算」通訊協定命令。 這些命令可修改資產的表示法，而不會破壞資產。

對於「影像伺服」,`urlModifier`參數中的命令會發佈在「修飾詞目錄」欄位中，並在請求URL上指定的任何命令之前套用。 `urlPostApplyModifier`中的命令將發佈到`PostModifier`目錄欄位，並將覆蓋請求URL或`urlModifier`中的任何命令。 對於「影像渲染」,`urlModifier`和`urlPostApplyModifier`中的命令將串連並發佈到「修飾詞目錄」欄位。

## 授權用戶類型{#section-fefcd732ccf64c78956606538f96c73d}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| `*`urlModifier`*` | `xsd:string` | 否 | 在請求或`urlPostApplyModifier`命令之前應用影像服務或影像渲染協定命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 否 | 在`urlModifier`和請求命令後套用的「影像伺服」或「影像演算」通訊協定命令。 |

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
