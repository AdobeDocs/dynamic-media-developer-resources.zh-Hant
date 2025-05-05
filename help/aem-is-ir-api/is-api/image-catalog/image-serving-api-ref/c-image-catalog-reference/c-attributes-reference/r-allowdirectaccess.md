---
description: 允許直接存取路徑型資產。
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

允許直接存取路徑型資產。

定義此屬性時，會根據使用`include`或`exclude`關鍵字，允許或限制指定物件型別的路徑型存取。

>[!NOTE]
>
>如果未指定`AllowDirectAccess`屬性，預設值為`exclude`。

* `include`允許存取指定的物件型別，並限制其他所有物件型別的存取權。
* `exclude`會限制指定物件型別的存取權，並允許其他所有型別的存取權。

如果未指定`include`或`exclude`，則假設為`include`。

可以控制下列型別：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 範例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 只允許直接存取`IS`和`STATIC`物件型別

  `AllowDirectAccess=include:IS,STATIC`

* 允許直接存取`IS`和`STATIC` `AllowDirectAccess=exclude:IS,STATIC`以外的所有物件型別

* 允許直接存取&#x200B;*no*&#x200B;物件型別（亦即，不包含任何物件）

  `AllowDirectAccess=include:`

* 允許直接存取&#x200B;*所有*&#x200B;物件型別（亦即，不排除任何物件）

  `AllowDirectAccess=exclude:`

* 相當於`include:IS,STATIC` （若不存在`include`/ `exclude`，則假設為`include`）

  `AllowDirectAccess=IS,STATIC`

  請注意，如果未針對此公司指定`AllowDirectAccess`屬性，則使用此預設值。

* 不包含任何專案，相當於`include:` （如果沒有`include`/ `exclude`，則假設為`include`）

  `AllowDirectAccess=`
