---
description: 建立影像格式。
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# saveImageFormat{#saveimageformat}

建立影像格式。

>[!NOTE]
>
>`urlModifier`欄位值必須包含有效的XML。 例如，將`&`變更為`&`。 從IPS用戶介面獲取`urlModfier`值。

## 授權的使用者類型 {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**輸入(saveImageFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 使用您要使用的影像格式的公司控制代碼。 |
| `*`imageFormatHandle`*` | `xsd:string` | 否 | 要保存的影像格式句柄。 |
| `*`名稱`*` | `xsd:string` | 是 | 影像格式名稱。 |
| `*`urlModifier`*` | `xsd:string` | 是 | 這可以是任何IPS協定查詢字串。 要產生URL修飾詞，最簡單的方式是使用IPS使用者介面建立修飾詞，然後剪下並貼上查詢字串。 |

**輸出(saveImageFormatReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`imageFormatHandle`*` | `xsd:string` | 是 | 處理影像格式。 |

## 範例 {#section-c7bd733212ef494297a97093f3af193f}

此程式碼範例會建立影像格式。 在此示例中，`urlModifier`由其在IPS用戶介面中的值確定，該介面具有有效的HTML格式。

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
