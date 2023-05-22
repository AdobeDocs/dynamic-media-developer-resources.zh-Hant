---
description: 允許直接訪問基於路徑的資產。
solution: Experience Manager
title: 允許直接訪問
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 允許直接訪問{#allowdirectaccess}

允許直接訪問基於路徑的資產。

定義此屬性時，將允許或限制指定對象類型的基於路徑的訪問，具體取決於 `include` 或 `exclude` 關鍵字。

>[!NOTE]
>
>如果 `AllowDirectAccess` 未指定屬性，預設值為 `exclude`。

* `include` 允許訪問指定的對象類型，並限制所有其他對象的訪問。
* `exclude` 限制對指定對象類型的訪問，並允許對其他所有對象的訪問。

如果兩者都不 `include` 無 `exclude` 已指定， `include` 假設。

可以控制以下類型：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 範例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 僅允許直接訪問 `IS` 和 `STATIC` 對象類型

   `AllowDirectAccess=include:IS,STATIC`

* 允許直接訪問除外的所有對象類型 `IS` 和 `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* 允許直接訪問 *不* 對象類型（即不包括無）

   `AllowDirectAccess=include:`

* 允許直接訪問 *全部* 對象類型（即無排除）

   `AllowDirectAccess=exclude:`

* 相當於 `include:IS,STATIC` （如果） `include`/ `exclude` 沒有， `include` 假定)

   `AllowDirectAccess=IS,STATIC`

   請注意，在 `AllowDirectAccess` 未為此公司指定屬性。

* 包括無，等於 `include:` （如果） `include`/ `exclude` 沒有， `include` 假定)

   `AllowDirectAccess=`
