---
description: 地址篩選元素。 在<rule>和<pathrule>元素中為可選。
solution: Experience Manager
title: 地址篩選器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 7%

---

# 地址篩選器{#addressfilter}

地址篩選元素。 在`<rule>`和`<pathrule>`元素中為可選。

套用規則時覆寫`attribute::ClientAddressFilter`。

## 屬性 {#section-31e9ad29e9934933ac154bccbc729172}

無。

## 資料 {#section-c762bdfe425140d689ea5abf25e9a48a}

IP位址清單（以逗號分隔）。 每個單個地址可以包括可選的網路掩碼尾碼，以允許指定IP地址範圍。 如需詳細資訊，請參閱`attribute::ClientAddressFilter`。

## 說明 {#section-d561b2485e004ef8a2085997d0f4bca6}

通過在`<addressfilter>`元素中指定此映像目錄，可以限制對一個或多個特定客戶端IP地址的訪問。 如果客戶端IP地址不匹配，則返回「拒絕請求」錯誤。

如果`<addressfilter>`為空或未指定，則不限制訪問。

如果`<rule>`元素中的`<expression>`不存在或為空，則`<addressfilter>`會套用至所有請求。

## 另請參閱 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[屬性：:ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
