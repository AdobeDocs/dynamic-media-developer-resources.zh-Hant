---
description: 設定指定資產的「影像服務」或「影像呈現」協定命令。 這些命令可修改資產的表示形式，而不會破壞它。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

設定指定資產的「影像服務」或「影像呈現」協定命令。 這些命令可修改資產的表示形式，而不會破壞它。

對於影像服務， `urlModifier` 參數將發佈在「修改量目錄」欄位中，並在請求URL上指定的任何命令之前應用。 命令 `urlPostApplyModifier` 已發佈到 `PostModifier` 目錄欄位，並覆蓋請求URL或中的任何命令 `urlModifier`。 對於影像渲染， `urlModifier` 和 `urlPostApplyModifier` 並發佈到「修改量目錄」欄位。

## 授權用戶類型 {#section-fefcd732ccf64c78956606538f96c73d}

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
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| 資產句柄 | `xsd:string` | 是 | 資產句柄。 |
| url修飾符 | `xsd:string` | 否 | 在請求或 `urlPostApplyModifier` 的雙曲餘切值。 |
| urlPostApplyModifier | `xsd:string` | 否 | 在以下時間後應用的影像服務或影像呈現協定命令 `urlModifier` 命令。 |

**輸出(setUrlModifierReturn)**

IPS API不會為此操作返迴響應。

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
