---
description: 傳回所有公司的陣列。
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# getAllCompanies{#getallcompanies}

傳回所有公司的陣列。

語法

## 授權的使用者類型 {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## 參數 {#section-efd74992e6904ebabe7383b577af4fdb}

**輸入(getAllCompaniesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`includeExpired`*` | `xsd:boolean` | 是 | 設為true ，可傳回過期和未過期的公司。 |

**輸出(getAllCompaniesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyArray`*` | `types:CompanyArray` | 是 | 公司的陣列。 |

## 範例 {#section-3eecf4e6900b41fb92a0e3214791c6b9}

此程式碼範例會傳回陣列中IPS中的所有公司。 請注意，為了簡單起見，範例回應會遭截斷。

**請求**

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**回答**

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```
