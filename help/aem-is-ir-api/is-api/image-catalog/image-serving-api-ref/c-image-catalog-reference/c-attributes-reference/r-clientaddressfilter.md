---
description: 客戶端IP地址篩選器。 允許指定一個或多個IP地址或地址範圍。
solution: Experience Manager
title: 客戶端地址篩選器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# 客戶端地址篩選器{#clientaddressfilter}

客戶端IP地址篩選器。 允許指定一個或多個IP地址或地址範圍。

如果指定，則拒絕從未列出IP地址的客戶端發出的對此映像目錄的請求。

## 屬性 {#section-d785265988324af68835410c9ba54147}

以逗號分隔的IP地址清單（使用CIDR表示法）:

`*`ip地址`*` `[`/ *`netmask`*`]`&#42; `[`。*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ip地址</span> </p> </td> 
  <td class="stentry"> <p>IP地址 <span class="varname"> ddd.ddd.ddd.ddd.ddd</span> 的子菜單。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 網路掩碼</span> </p></td> 
  <td class="stentry"> <p>淨掩碼(0...32)。 </p></td> 
 </tr> 
</table>

當預處理規則與 `<addressfilter>` 元素。

## 預設 {#section-de26e8c9225745e985e4beac1f03f4f6}

繼承自 `default::AddressFilter` 或為空。

## 範例 {#section-a955314d2b6a4213a16c12a8b18d8627}

無訪問限制： `0.0.0.0/0`

授予從192開始的所有地址的訪問權限： `192.0.0.0/8`

授予對地址介於192.168.12.0和192.168.13.255之間的512台主機的訪問權限： `192.168.12.0/23`

授予對單個IP地址的訪問權限： `192.168.2.117` 或 `192.168.2.117/32`

## 另請參閱 {#section-4ea89a7d82e14a4a800487d2d8801465}

[地址篩選器](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
