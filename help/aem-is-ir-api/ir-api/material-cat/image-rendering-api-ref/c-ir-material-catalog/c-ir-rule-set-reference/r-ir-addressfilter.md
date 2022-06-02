---
description: 地址篩選器元素。 可選 <rule> 元素。 應用規則時覆蓋屬性ClientAddressFilter。
solution: Experience Manager
title: 地址篩選器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# 地址篩選器{#addressfilter}

地址篩選器元素。 可選 `<rule>` 元素。 應用規則時覆蓋屬性：:ClientAddressFilter。

## 屬性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

無。

## 資料 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

以逗號分隔的IP地址清單。 每個單獨的地址可包括可選的網路掩碼尾碼以允許IP地址範圍的規範。 請參閱 [屬性：:ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) 的雙曲餘切值。

## 說明 {#section-099b7839c4be40c68cbff29dad14e7d5}

通過在 `<addressfilter>` 的子菜單。 如果客戶端IP地址不匹配，則會向客戶端返回「請求拒絕」錯誤。

如果 `<addressfilter>` 為空或未指定。

如果 `<expression>` 的 `<rule>` 元素不存在或為空， `<addressfilter>` 應用於所有請求。

`localhost` 總是隱式的 `ClientAddressFilter` 定義，即使未明確指定。 源自 `localhost` 不會被拒絕，不管 `ClientAddressFilter` 規範。

## 西阿也 {#section-02056065e0c042e1b155b2f3e5b84ef7}

[屬性：:ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
