---
description: 可讓管理員建立新的元資料欄位，以便與內容管理系統或模板操作協調。 建立的元資料欄位的範例包括關鍵字、關於影像作者的資訊或版權持有人資訊。
solution: Experience Manager
title: createMetadataField
feature: Dynamic Media Classic,SDK/API，中繼資料
role: Developer,Administrator
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 13%

---

# createMetadataField{#createmetadatafield}

可讓管理員建立新的元資料欄位，以便與內容管理系統或模板操作協調。 建立的元資料欄位的範例包括關鍵字、關於影像作者的資訊或版權持有人資訊。

語法

## 授權的使用者類型 {#section-2f61d79f8cac4692bfa53b95035ddd89}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 中繼資料欄位所屬的公司名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 資產類型. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 您要建立的中繼資料欄位名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">中繼資料欄位類型。 <p>中繼資料欄位類型常數會定義可用類型。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>要建立的元資料欄位的預設值（例如<span class="codeph"> Scene 7</span>）。 </p> <p>標籤欄位類型不支援預設值，且必須省略。 如果為標籤欄位類型指定非空的預設值，則會傳回錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 隱藏或公開IPS系統特定元資料。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>布林值標幟，指出設定值時是否強制（驗證）中繼資料欄位。 </p> <p>如果設為true，則如果在<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>中設定了非法值，則會擲回錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 可讓您建立一組所選標籤可指向的共用枚舉值。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(createMetadataFieldReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | 是 | 新中繼資料欄位的控點。 |

## 範例 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

此代碼示例建立名為`createMetadataField`的字串類型元資料欄位。 回應會將控點傳回新中繼資料欄位。

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
