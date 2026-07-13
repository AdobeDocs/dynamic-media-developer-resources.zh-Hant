---
description: 使用資產控制代碼清單陣列將檔案分組到組中。
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
TQID: 'https://experienceleague.adobe.com/YHElzYMAYDta1hG2th30GNuz2IgFmN5OTUPx63K1p9o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 4%

---

# [!DNL AutomatedSetGenerationJob]{#automatedsetgenerationjob}

使用資產控制代碼清單陣列將檔案分組到組中。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：HandleArray</span> </td> 
   <td colname="col3">用來建立該集的資產控制代碼陣列。 <p>依預設，1000是您可以在陣列中擁有的最大資產數量。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL destFolder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 要儲存集合的資料夾路徑。 依預設儲存至公司根資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3"> 設定旗標以指出是否應該發佈資產。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL autoSetCreationOptions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：AutoSetCreationOptions</span> </td> 
   <td colname="col3">您可以在上傳檔案上執行的一組產生程式檔陣列。 請參閱<a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>為工作設定自動電子郵件通知。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**電子郵件設定選項**

`emailSetting`引數包含下列選項：

| 選項 | 傳回 |
|---|---|
| `All` | 所有工作通知（錯誤、警告、完成）給指定的收件者。 |
| `Error` | 指定的收件者發生工作錯誤。 |
| `ErrorAndWarning` | 給指定收件者的工作錯誤和警告。 |
| `JobCompletion` | 給指定收件者的工作完成通知。 |
| `None` | 工作未將任何工作通知傳送給指定的收件者。 |

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

