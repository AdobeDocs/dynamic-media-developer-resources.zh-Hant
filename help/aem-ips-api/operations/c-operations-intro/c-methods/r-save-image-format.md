---
description: 建立影像格式。
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 12%

---

# saveImageFormat{#saveimageformat}

建立影像格式。

>[!NOTE]
>
>的 `urlModifier` 欄位值必須由有效的XML組成。 例如，更改 `&` 至 `&`。 獲取 `urlModfier` IPS用戶介面中的值。

## 授權用戶類型 {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**輸入(saveImageFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 要使用的影像格式的公司的句柄。 |
| imageFormatHandle | `xsd:string` | 否 | 要保存的影像格式句柄。 |
| 名稱 | `xsd:string` | 是 | 影像格式名稱。 |
| url修飾符 | `xsd:string` | 是 | 這可以是任何IPS協定查詢字串。 生成URL修飾符的最簡單方法是使用IPS用戶介面建立URL修飾符，然後剪切並貼上查詢字串。 |

**輸出(saveImageFormatReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | 是 | 影像格式的句柄。 |

## 範例 {#section-c7bd733212ef494297a97093f3af193f}

此代碼示例建立影像格式。 在本例中， `urlModifier` 是由其在IPS用戶介面中的值所決定的，具有有效的HTML格式。

**請求**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**回答**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```
