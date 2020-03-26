---
description: 用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。
seo-description: 用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a557795-0caf-4b5f-974e-fb4c1481a83c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。

指定時，會拒絕從未列出IP位址的客戶端發出的對此映像目錄的請求。

## 屬性 {#section-d785265988324af68835410c9ba54147}

IP地址的逗號分隔清單(使用可選網路掩碼（CIDR表示法）:

`*`ipAddress`*``[`*`netmask`*`]`/`[`**`ipAddress`*,`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>IP位址 <span class="varname"> 為ddd.ddd.ddd</span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 網路掩碼</span> </p></td> 
  <td class="stentry"> <p>淨遮色片(0...32)。 </p></td> 
 </tr> 
</table>

套用含元素的預處理規則時，會忽 `<addressfilter>` 略此屬性。

## 預設 {#section-de26e8c9225745e985e4beac1f03f4f6}

繼承自 `default::AddressFilter` （如果未定義或為空）。

## 範例 {#section-a955314d2b6a4213a16c12a8b18d8627}

無存取限制： `0.0.0.0/0`

授予對所有地址（從192開始）的訪問權限： `192.0.0.0/8`

授予對地址介於192.168.12.0和192.168.13.255之間的512台主機的訪問權： `192.168.12.0/23`

授予對單個IP地址的訪問權： `192.168.2.117` 或 `192.168.2.117/32`

## 另請參閱 {#section-4ea89a7d82e14a4a800487d2d8801465}

[地址篩選](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
