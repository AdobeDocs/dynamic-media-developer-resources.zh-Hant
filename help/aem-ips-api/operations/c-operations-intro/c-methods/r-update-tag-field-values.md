---
description: 更新標籤欄位的標籤字典值。
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 6de49217-2d15-49d9-9357-b058b2564686
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 15%

---

# updateTagFieldValues{#updatetagfieldvalues}

更新標籤欄位的標籤字典值。

語法

## 授權的使用者類型 {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-0a3a4bab026746238c9d4009caf42e94}

**Input(updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要 </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 公司負責人。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 標籤欄位句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：TagValueUpdateArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">您要更新的標籤欄位值陣列。 <p>注意： 僅更新標籤字串值。 不會影響資產關聯。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(updateTagFieldValuesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功更新的標籤欄位數。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作嘗試更新標籤欄位時生成的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作嘗試更新標籤欄位時生成的錯誤數。 |
| `*`warningDetailArray`*` | `types:TagValueUpdateFaultArray` | 否 | 與資產相關聯的詳細資訊陣列，當操作嘗試更新標籤欄位時，資產會產生警告。 |
| `*`errorDetailArray`*` | `types:TagValueUpdateFaultArray` | 否 | 與嘗試更新標籤欄位時產生錯誤之資產相關聯的詳細資訊陣列。 |

## 範例 {#section-bb4dcf97044c4675974c9b8d27674001}

**請求**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**回答**

```java
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```
