---
description: 允許直接存取路徑型資產。
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

允許直接存取路徑型資產。

定義此屬性時，根據是使用`include`還是使用`exclude`關鍵字，允許或限制指定對象類型的基於路徑的訪問。

>[!NOTE]
>
>如果未指定`AllowDirectAccess`屬性，預設值為`exclude`。

* `include` 允許訪問指定的對象類型，並限制所有其他對象的訪問。
* `exclude` 限制對指定對象類型的訪問，並允許對其他所有對象進行訪問。

若未指定`include`或`exclude`，則假設`include`。

可以控制下列類型：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 範例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 僅允許對`IS`和`STATIC`對象類型進行直接訪問

   `AllowDirectAccess=include:IS,STATIC`

* 允許直接訪問除`IS`和`STATIC``AllowDirectAccess=exclude:IS,STATIC`之外的所有對象類型

* 允許直接訪問&#x200B;*no*&#x200B;對象類型（即不包括任何對象）

   `AllowDirectAccess=include:`

* 允許直接訪問&#x200B;*all*&#x200B;對象類型（即不排除任何對象）

   `AllowDirectAccess=exclude:`

* 等同於`include:IS,STATIC`（如果`include`/ `exclude`不存在，則假設`include`）

   `AllowDirectAccess=IS,STATIC`

   請注意，這是預設值，若未指定此公司的`AllowDirectAccess`屬性，則會使用此預設值。

* 包含無，等同於`include:`（如果`include`/ `exclude`不存在，則假設`include`）

   `AllowDirectAccess=`
