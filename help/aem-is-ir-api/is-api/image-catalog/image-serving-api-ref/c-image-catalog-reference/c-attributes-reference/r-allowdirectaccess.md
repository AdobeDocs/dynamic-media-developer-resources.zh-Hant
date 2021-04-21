---
description: 允許直接存取路徑型資產。
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

允許直接存取路徑型資產。

定義此屬性時，根據是否使用`include`或`exclude`關鍵字，允許或限制指定對象類型的基於路徑的訪問。

>[!NOTE]
>
>如果未指定`AllowDirectAccess`屬性，則預設值為`exclude`。

* `include` 允許對指定對象類型的訪問，並限制對所有其他對象類型的訪問。
* `exclude` 限制對指定對象類型的訪問，並允許對其他所有對象進行訪問。

如果未指定`include`或`exclude`，則假設`include`。

可以控制以下類型：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 範例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 僅允許直接訪問`IS`和`STATIC`對象類型

   `AllowDirectAccess=include:IS,STATIC`

* 允許直接訪問除`IS`和`STATIC``AllowDirectAccess=exclude:IS,STATIC`之外的所有對象類型

* 允許直接訪問&#x200B;*no*&#x200B;對象類型（即不包括）

   `AllowDirectAccess=include:`

* 允許直接訪問&#x200B;*所有*&#x200B;對象類型（即不排除任何）

   `AllowDirectAccess=exclude:`

* 等效於`include:IS,STATIC`（如果`include`/ `exclude`不存在，則假設`include`）

   `AllowDirectAccess=IS,STATIC`

   請注意，這是當未為此公司指定`AllowDirectAccess`屬性時使用的預設值。

* 包含none，相當於`include:`（如果`include`/ `exclude`不存在，則假設`include`）

   `AllowDirectAccess=`

