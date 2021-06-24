---
description: 為指定的資產設定「影像提供」或「影像呈現」協定命令。 這些命令會修改資產的表示，而不會破壞資產。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

為指定的資產設定「影像提供」或「影像呈現」協定命令。 這些命令會修改資產的表示，而不會破壞資產。

對於「影像伺服」， `urlModifier`參數中的命令會發佈在「修飾詞目錄」欄位中，並在請求URL上指定的任何命令之前套用。 `urlPostApplyModifier`中的命令將發佈到`PostModifier`目錄欄位，並將覆蓋請求URL或`urlModifier`中的任何命令。 針對影像呈現，`urlModifier`和`urlPostApplyModifier`中的命令會串連並發佈至修飾詞目錄欄位。

## 授權的使用者類型 {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Input(setUrlModifierParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| `*`urlModifier`*` | `xsd:string` | 否 | 要在請求或`urlPostApplyModifier`命令之前應用的影像伺服或影像呈現協定命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 否 | 要在`urlModifier`和請求命令之後應用的影像伺服或影像呈現協定命令。 |

**輸出(setUrlModifierReturn)**

IPS API不會針對此操作傳回回應。

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
