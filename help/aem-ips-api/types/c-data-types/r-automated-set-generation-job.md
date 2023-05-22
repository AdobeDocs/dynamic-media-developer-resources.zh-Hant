---
description: 使用資產句柄清單陣列將檔案分組到集中。
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 7%

---

# [!DNL AutomatedSetGenerationJob]{#automatedsetgenerationjob}

使用資產句柄清單陣列將檔案分組到集中。

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
   <td colname="col2"> <span class="codeph"> 類型：HandleArray</span> </td> 
   <td colname="col3">用於建立集的資產句柄陣列。 <p>預設情況下，1000是您在陣列中可以擁有的最大資產數。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL destFolder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 要保存集的資料夾的路徑。 預設情況下，保存到公司根資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 設定一個標誌以指示是否應發佈資產。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL autoSetCreationOptions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：自動設定建立選項</span> </td> 
   <td colname="col3">可以在上載的檔案上運行的一組集生成指令碼。 請參閱 <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> 自動集建立選項</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>設定作業的自動電子郵件通知。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**電子郵件設定選項**

的 `emailSetting` 參數包括以下選項：

| 選項 | 返回 |
|---|---|
| `All` | 指定收件人的所有作業通知（錯誤、警告、完成）。 |
| `Error` | 指定收件人的作業錯誤。 |
| `ErrorAndWarning` | 指定收件人的作業錯誤和警告。 |
| `JobCompletion` | 指定收件人的作業完成通知。 |
| `None` | 作業不會向指定的收件人發送任何作業通知。 |

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
