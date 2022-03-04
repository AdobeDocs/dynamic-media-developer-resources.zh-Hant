---
description: 允許管理員建立新的元資料欄位以與內容管理系統或模板操作協調。 建立的元資料欄位的示例包括關鍵字、關於影像作者的資訊或版權持有人資訊。
solution: Experience Manager
title: createMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 13%

---

# createMetadataField{#createmetadatafield}

允許管理員建立新的元資料欄位以與內容管理系統或模板操作協調。 建立的元資料欄位的示例包括關鍵字、關於影像作者的資訊或版權持有人資訊。

語法

## 授權用戶類型 {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## 參數 {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**輸入(createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 參數名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要 </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 公司名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 元資料欄位所屬的公司的名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 資產類型</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 資產類型. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 正在建立的元資料欄位的名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 欄位類型</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">元資料欄位類型。 <p>元資料欄位類型常數定義可用類型。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>要建立的元資料欄位的預設值(例如， <span class="codeph"> 場景7</span>)。 </p> <p>標籤欄位類型不支援預設值，必須省略。 如果為標籤欄位類型指定了非空預設值，則返回錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 隱藏</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 隱藏或公開IPS系統特定的元資料。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> 強制</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd：布爾</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>一個布爾標誌，指示在設定值時是否強制（驗證）元資料欄位。 </p> <p>如果設定為true，則如果在中設定了非法值，則會拋出錯誤 <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 初始標籤值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 允許您建立一組共用枚舉值，選定標籤可以指向這些值。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(createMetadataFieldReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`欄位句柄`*` | `xsd:string` | 是 | 新元資料欄位的句柄。 |

## 範例 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

此代碼示例建立名為的字串類型元資料欄位 `createMetadataField`。 響應將句柄返回到新元資料欄位。

**請求**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**回答**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```
