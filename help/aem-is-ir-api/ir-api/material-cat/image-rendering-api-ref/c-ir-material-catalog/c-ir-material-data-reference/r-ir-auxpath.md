---
description: 資料檔案路徑。 與此映像關聯的非映像資料檔案的相對路徑和名稱。
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# AuxPath{#auxpath}

資料檔案路徑。 與此映像關聯的非映像資料檔案的相對路徑和名稱。

伺服器將此值與屬性：:RootPath結合，以生成實際檔案路徑。 也可以是絕對檔案路徑。

用於為機櫃材料指定機櫃樣式檔案或為窗口覆蓋材料指定窗口覆蓋樣式檔案。 保留空白以表示所有其他材料。

## 屬性 {#section-4268350054b7421da0ce0327f0731a52}

文字字串值。 如果指定，則必須是有效的相對或絕對檔案路徑。 需要使用機櫃材料和窗蓋材料。 對於所有其它材料必須為空。

## 預設 {#section-287005c2d8e948fa958f69ba7b90b437}

無。

## 另請參閱 {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
