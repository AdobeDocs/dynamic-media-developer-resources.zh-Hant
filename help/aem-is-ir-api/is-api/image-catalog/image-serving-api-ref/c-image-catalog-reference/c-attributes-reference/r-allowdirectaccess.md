---
description: 允許直接存取路徑型資產。
seo-description: 允許直接存取路徑型資產。
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AllowDirectAccess{#allowdirectaccess}

允許直接存取路徑型資產。

定義此屬性時，根據是否使用或關鍵字，指定的對象類型允許或限制基於路 `include` 徑 `exclude` 的訪問。

>[!NOTE]
>
>如果未 `AllowDirectAccess` 指定屬性，則預設值為 `exclude`。

* `include` 允許對指定對象類型的訪問，並限制對所有其他對象類型的訪問。
* `exclude` 限制對指定對象類型的訪問，並允許對其他所有對象進行訪問。

若未指 `include` 定 `exclude` 或未指定， `include` 則假設。

可以控制以下類型：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 範例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 僅允許直接訪問 `IS` 和對 `STATIC` 像類型

   `AllowDirectAccess=include:IS,STATIC`

* 允許直接訪問除和之外的所有對象類型 `IS` 。 `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* 允許直接訪 *問* no對象類型（即不包括任何對象）

   `AllowDirectAccess=include:`

* 允許直接訪 *問所有* 對象類型（即不排除無）

   `AllowDirectAccess=exclude:`

* 等同 `include:IS,STATIC` 於(若 `include`/ `exclude` 不存在，則假 `include` 設為)

   `AllowDirectAccess=IS,STATIC`

   請注意，這是當未為此公司指定屬 `AllowDirectAccess` 性時使用的預設值。

* 包含無，等 `include:` 同於(如 `include`果/ `exclude` 不存在，則假 `include` 設為)

   `AllowDirectAccess=`

