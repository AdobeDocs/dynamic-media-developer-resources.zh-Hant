---
description: HTTP回應標題元素。 在<rule>元素中為選用。
solution: Experience Manager
title: header
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 4%

---

# 標題{#header}

HTTP回應標題元素。 `<rule>`元素中為可選。

## 屬性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** :必填。指定HTTP標頭的名稱。

**`Action`= &quot;set&quot; |`"add"`**:選填。預設值為`"set"`，會取代任何目前的標題值。 指定`"add"`以附加標題值，並以逗號分隔。

## 資料 {#section-a387f541396c49d99c29692a38032914}

標題值。

## 說明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

允許新增HTTP回應標題，以及新增或取代預先定義標題的值。 名稱和值必須符合HTTP標準。 不會套用其他編碼。

影像伺服替代變數可用於標題名稱和標題值中。 這可讓您控制請求中的兩個字串。

## 範例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

當請求中將標題值指定為變數時，下列規則會套用自訂標題：

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

此規則由下列請求觸發，並設定HTTP回應標題`Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
