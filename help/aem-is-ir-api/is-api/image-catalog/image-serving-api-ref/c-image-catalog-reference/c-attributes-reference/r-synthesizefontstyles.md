---
title: 合成字型樣式
description: 啟用合成字型變體。 控制如果請求但在字型映射中找不到該樣式，則伺服器是否應生成錯誤響應或合成粗體、斜體或粗體/斜體字型樣式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---

# 合成字型樣式{#synthesizefontstyles}

啟用合成字型變體。 控制如果請求但在字型映射中找不到該樣式，則伺服器是否應生成錯誤響應或合成粗體、斜體或粗體/斜體字型樣式。

>[!NOTE]
>
>合成字型樣式通常會導致對此類樣式使用實際字型的效果較差。

## 屬性 {#section-3205560a74774ebf9c916b07bd15aca6}

標幟. 設定為0可禁用，設定為1可啟用合成字型樣式。

## 預設 {#section-71f94aa65e404d14b441674c040b59e3}

繼承自 `default::SynthesizeFontStyles` 或為空。

## 另請參閱 {#section-47a79659cc844272b6d5f36c946e12ac}

[字型映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
