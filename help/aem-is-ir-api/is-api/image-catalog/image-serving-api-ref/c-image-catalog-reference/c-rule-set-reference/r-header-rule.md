---
description: HTTP響應頭元素。 可選 <rule> 元素。
solution: Experience Manager
title: header
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# 標題{#header}

HTTP響應頭元素。 可選 `<rule>` 元素。

## 屬性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*文本*&quot;** :必需。 指定HTTP標頭的名稱。

**`Action`= &quot;設定&quot; |`"add"`**:可選。 預設值為 `"set"`，將替換任何當前標題值。 指定 `"add"` 添加標題值，用逗號分隔。

## 資料 {#section-a387f541396c49d99c29692a38032914}

標題值。

## 說明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

允許添加新的HTTP響應標頭，以及添加或替換預定義標頭的值。 名稱和值必須符合HTTP標準。 未應用其他編碼。

Image Service替代變數可用於標題名稱和標題值。 這允許從請求控制兩個字串。

## 範例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

當請求中將標頭值指定為變數時，以下規則將應用自定義標頭：

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

此規則由以下請求觸發，設定HTTP響應標頭 `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
