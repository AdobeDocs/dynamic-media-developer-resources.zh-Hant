---
description: 地址篩選元素。 在<rule>和<pathrule>元素中為可選項。
seo-description: 地址篩選元素。 在<rule>和<pathrule>元素中為可選項。
seo-title: 地址篩選
solution: Experience Manager
title: 地址篩選
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 6%

---


# 地址篩選器{#addressfilter}

地址篩選元素。 在`<rule>`和`<pathrule>`元素中為可選項。

在套用規則時覆寫`attribute::ClientAddressFilter`。

## 屬性 {#section-31e9ad29e9934933ac154bccbc729172}

無。

## 資料 {#section-c762bdfe425140d689ea5abf25e9a48a}

IP位址的逗號分隔清單。 每個單獨地址可包括可選網路掩碼尾碼以允許指定IP地址範圍。 如需詳細資訊，請參閱`attribute::ClientAddressFilter`。

## 說明 {#section-d561b2485e004ef8a2085997d0f4bca6}

在`<addressfilter>`元素中指定此映像目錄的訪問權限可以限制為一個或多個特定客戶機IP地址。 如果客戶端IP位址不相符，則會傳回「請求拒絕」錯誤給客戶端。

如果`<addressfilter>`為空或未指定，則不限制訪問。

如果`<rule>`元素中的`<expression>`不存在或為空，則`<addressfilter>`將應用於所有請求。

## 另請參閱 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[屬性：:ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
