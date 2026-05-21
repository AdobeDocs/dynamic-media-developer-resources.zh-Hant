---
description: 屬性集型別指定用來協助管理屬性集的各種設定。
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
TQID: 'https://experienceleague.adobe.com/JOAxK9j-P0v8inQRU65C2rVCM9-OnXTXCF6wtp6eksY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 10%

---

# createPropertySetType{#createpropertysettype}

屬性集型別指定用來協助管理屬性集的各種設定。

語法

## 授權的使用者型別 {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-43dece72eb9f44df80f4a119dd2c008b}

**輸入(createPropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 擁有屬性集型別的公司的控制代碼。 如果未傳遞`companyHandle`，且呼叫者為`IpsAdmin`，則會建立全域屬性集型別。 |
| name | `xsd:string` | 是 | 屬性集型別的名稱。 |
| propertyType | `xsd:string` | 是 | 屬性集型別的選擇。 |
| allowmultiple | `xsd:boolean` | 是 | 決定您的程式是否可以擁有多個屬性集。 |

**輸出(createPropertySetTypeReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| typeHandle | `xsd:string` | 是 | 型別的控制代碼。 |

## 範例 {#section-13396c9639a6475190e622eae3cdb534}

這個程式碼範例會以`PropertySet Types`常數所指定的名稱和型別建立屬性集。 擁有屬性集型別的公司的控制代碼。 如果未傳遞companyHandle且呼叫者是IpsAdmin，則會建立全域屬性集型別。

**要求**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**回應**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```
