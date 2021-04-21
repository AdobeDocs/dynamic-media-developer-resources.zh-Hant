---
description: 用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---


# ClientAddressFilter{#clientaddressfilter}

用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。

指定時，會拒絕從未列出IP位址的客戶端發出的對此映像目錄的請求。

## 屬性 {#section-d785265988324af68835410c9ba54147}

IP地址的逗號分隔清單(使用可選網路掩碼（CIDR表示法）:

`*`ipAddress`*` `[`/  *`netmask`*`]`* `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> ddd.ddd.ddd.ddd</span>格式的IP位址。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 網路掩碼</span> </p></td> 
  <td class="stentry"> <p>淨遮色片(0...32)。 </p></td> 
 </tr> 
</table>

套用含`<addressfilter>`元素的預處理規則時，會忽略此屬性。

## 預設 {#section-de26e8c9225745e985e4beac1f03f4f6}

如果未定義或為空，則繼承自`default::AddressFilter`。

## 範例 {#section-a955314d2b6a4213a16c12a8b18d8627}

無存取限制：`0.0.0.0/0`

授予對所有地址（從192開始）的訪問權限：`192.0.0.0/8`

授予對地址介於192.168.12.0和192.168.13.255之間的512台主機的訪問權：`192.168.12.0/23`

授予對單個IP地址的訪問權：`192.168.2.117`或`192.168.2.117/32`

## 另請參閱 {#section-4ea89a7d82e14a4a800487d2d8801465}

[地址篩選](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
