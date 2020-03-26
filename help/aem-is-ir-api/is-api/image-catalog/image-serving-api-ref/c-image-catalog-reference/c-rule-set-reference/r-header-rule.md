---
description: HTTP回應標題元素。 在<rule>元素中為可選項。
seo-description: HTTP回應標題元素。 在<rule>元素中為可選項。
seo-title: header
solution: Experience Manager
title: header
topic: Scene7 Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# header{#header}

HTTP回應標題元素。 在元素中為 `<rule>` 選用。

## 屬性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;**:必要。 指定HTTP標題的名稱。

**`Action`= &quot;set&quot;|`"add"`**:可選。 預設值`"set"`為，會取代任何目前的標題值。 指定`"add"`要附加標題值，以逗號分隔。

## 資料 {#section-a387f541396c49d99c29692a38032914}

標題值。

## 說明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

允許新增HTTP回應標題，以及新增或取代預先定義標題的值。 名稱和值必須符合HTTP標準。 不會套用其他編碼。

「影像伺服」替代變數可用於標題名稱和標題值。 這可讓您控制來自請求的兩個字串。

## 範例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

當在請求中指定標題值為變數時，下列規則會套用自訂標題：

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

此規則由下列請求觸發，設定HTTP回應標題 `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
