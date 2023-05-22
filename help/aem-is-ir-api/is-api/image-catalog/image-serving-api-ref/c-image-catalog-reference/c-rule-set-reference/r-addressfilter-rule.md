---
description: 地址篩選器元素。 可選 <rule> 和 <pathrule> 元素。
solution: Experience Manager
title: 地址篩選器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# 地址篩選器{#addressfilter}

地址篩選器元素。 可選 `<rule>` 和 `<pathrule>` 元素。

覆蓋 `attribute::ClientAddressFilter` 。

## 屬性 {#section-31e9ad29e9934933ac154bccbc729172}

無。

## 資料 {#section-c762bdfe425140d689ea5abf25e9a48a}

以逗號分隔的IP地址清單。 每個單獨的地址可包括可選的網路掩碼尾碼以允許IP地址範圍的規範。 如需詳細資訊，請參閱`attribute::ClientAddressFilter`。

## 說明 {#section-d561b2485e004ef8a2085997d0f4bca6}

通過在 `<addressfilter>` 的子菜單。 如果客戶端IP地址不匹配，則會向客戶端返回「請求拒絕」錯誤。

如果 `<addressfilter>` 為空或未指定。

如果 `<expression>` 的 `<rule>` 元素不存在或為空， `<addressfilter>` 應用於所有請求。

## 另請參閱 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[屬性：:ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
