---
description: 位址篩選器元素。 <rule>和<pathrule>元素中的選用專案。
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# addressfilter{#addressfilter}

位址篩選器元素。 `<rule>`和`<pathrule>`專案中的選用專案。

套用規則時覆寫`attribute::ClientAddressFilter`。

## 屬性 {#section-31e9ad29e9934933ac154bccbc729172}

無。

## 資料 {#section-c762bdfe425140d689ea5abf25e9a48a}

IP位址的逗號分隔清單。 每個個別位址都可包含選用的網路遮罩尾碼，以便指定IP位址範圍。 如需詳細資訊，請參閱`attribute::ClientAddressFilter`。

## 說明 {#section-d561b2485e004ef8a2085997d0f4bca6}

在`<addressfilter>`元素中指定這些位址，可限制存取此影像目錄，使其只能存取一或多個特定使用者端IP位址。 如果使用者端IP位址不符，則會傳回「已拒絕要求」錯誤給使用者端。

如果`<addressfilter>`為空白或未指定，則不會限制存取。

如果`<rule>`專案中的`<expression>`不存在或空白，則會將`<addressfilter>`套用至所有要求。

## 另請參閱 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute：：ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
