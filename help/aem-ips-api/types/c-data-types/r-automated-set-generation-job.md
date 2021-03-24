---
description: 使用資產控制代碼清單陣列將檔案分組為一組。
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 7%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

使用資產控制代碼清單陣列將檔案分組為一組。

語法

## 參數 {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：HandleArray</span> </td> 
   <td colname="col3">用於建立集的資產句柄陣列。 <p>依預設，1000是您在陣列中可擁有的資產數目上限。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 要保存集的資料夾的路徑。 依預設，會儲存至公司根資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 設定旗標以指出資產是否應發佈。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AutoSetCreationOptions</span> </td> 
   <td colname="col3">可在上傳檔案上執行的一組集合層代指令碼。 請參閱<a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>為工作設定自動化電子郵件通知。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting選項**

`emailSetting`參數包含下列選項：

| 選項 | 退貨 |
|---|---|
| `All` | 指定收件者的所有工作通知（錯誤、警告、完成）。 |
| `Error` | 指定收件者的工作錯誤。 |
| `ErrorAndWarning` | 指定收件者的工作錯誤和警告。 |
| `JobCompletion` | 指定收件人的作業完成通知。 |
| `None` | 作業不會傳送任何作業通知給指定的收件者。 |

## 範例 {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```

