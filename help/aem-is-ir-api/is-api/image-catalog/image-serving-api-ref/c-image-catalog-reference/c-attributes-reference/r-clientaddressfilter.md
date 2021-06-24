---
description: 客戶端IP地址篩選器。 允許規範一個或多個IP地址或地址範圍。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

客戶端IP地址篩選器。 允許規範一個或多個IP地址或地址範圍。

指定後，對此映像目錄的請求將被拒絕，這些請求源自於位於未列出IP地址的客戶端。

## 屬性 {#section-d785265988324af68835410c9ba54147}

以逗號分隔的IP位址清單，含選用的網路遮罩（使用CIDR標籤法）:

`*`ipAddress`*` `[` /  *`netmask`*`]`*  `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> ddd.ddd.ddd.ddd</span>格式的IP地址。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 網路掩碼</span> </p></td> 
  <td class="stentry"> <p>淨掩碼(0...32)。 </p></td> 
 </tr> 
</table>

套用含`<addressfilter>`元素的預處理規則時，會忽略此屬性。

## 預設 {#section-de26e8c9225745e985e4beac1f03f4f6}

如果未定義或為空，則從`default::AddressFilter`繼承。

## 範例 {#section-a955314d2b6a4213a16c12a8b18d8627}

無訪問限制：`0.0.0.0/0`

授予從192開始的所有地址的訪問權：`192.0.0.0/8`

授予對地址介於192.168.12.0和192.168.13.255之間的512台主機的訪問權：`192.168.12.0/23`

授予對單一IP位址的存取權：`192.168.2.117`或`192.168.2.117/32`

## 另請參閱 {#section-4ea89a7d82e14a4a800487d2d8801465}

[地址篩選器](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
