---
title: header
description: HTTP回應標頭元素。 <rule>元素中的選用專案。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# header{#header}

HTTP回應標頭元素。 `<rule>`個元素中的選用專案。

## 屬性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*文字*&quot;** ：必要。 指定HTTP標頭的名稱。

**`Action`= &quot;set&quot; |`"add"`**：選擇性。 預設值為`"set"`，會取代任何目前的標頭值。 指定`"add"`以便附加標頭值（以逗號分隔）。

## 資料 {#section-a387f541396c49d99c29692a38032914}

標頭值。

## 說明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

允許新增新的HTTP回應標題，以及新增或取代預先定義標題的值。 名稱和值必須符合HTTP標準。 不會套用其他編碼。

「影像伺服」替代變數可用於標頭名稱和標頭值。 這可讓您從要求中控制兩個字串。

## 範例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

當請求中的標頭值指定為變數時，下列規則會套用自訂標頭：

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

此規則是由下列要求觸發，設定HTTP回應標頭`Edge-Control::no-store`：

`http://server/is/image/cat/id?$Edge-Control=no-store`
