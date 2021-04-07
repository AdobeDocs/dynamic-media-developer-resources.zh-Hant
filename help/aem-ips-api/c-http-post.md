---
description: 將資產上傳至Dynamic Media經典網站，涉及一或多個HTTPPOST請求，這些請求會設定工作，以協調與上傳檔案相關的所有記錄活動。
solution: Experience Manager
title: 透過HTTP POST上傳資產至UploadFile Servlet
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
translation-type: tm+mt
source-git-commit: e7c747c44d27ed1769ab872d962a814d80c0b345
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 3%

---

# 透過HTTP POST上傳資產至UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

將資產上傳至Dynamic Media經典網站，涉及一或多個HTTPPOST請求，這些請求會設定工作，以協調與上傳檔案相關的所有記錄活動。

使用下列URL存取UploadFile Servlet:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>上傳作業的所有POST請求都必須源自相同的IP位址。

**Dynamic Media地區的存取URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理位置 </p> </th> 
   <th colname="col2" class="entry"> <p>生產URL </p> </th> 
   <th colname="col3" class="entry"> <p>測試URL（用於預製開發和測試） </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>北美洲 </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>歐洲、中東、亞洲 </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本／亞太地區 </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## 上傳工作的工作流程{#section-873625b9512f477c992f5cdd77267094}

上傳工作由一或多個使用公用`jobHandle`將處理關聯至相同工作的HTTP POST組成。 每個請求都編碼為`multipart/form-data`，並由下清單單部分組成：

>[!NOTE]
>
>上傳作業的所有POST請求都必須源自相同的IP位址。

|  HTTPPOST表單部分  |  說明  |
|---|---|
| `auth`  |   必要. XML authHeader檔案，指定驗證和用戶端資訊。 請參閱[SOAP](/help/aem-ips-api/c-wsdl-versions.md)下的&#x200B;**請求驗證**。 |
| `file params`  |   選擇性. 您可以包含一或多個檔案，以便隨每個POST請求上傳。 如果未指定`uploadPostParams/fileName`參數，則每個檔案部分都可以在Content-Disposition標頭中包含檔案名參數，該參數將用作IPS中的目標檔案名。 |

|  HTTPPOST表單部分   |  uploadPostParams元素名稱   |  類型   |  說明   |
|---|---|---|---|
| `uploadParams` (必要. XML `uploadParams`檔案，指定上傳參數)   |   `companyHandle`  |  `xsd:string`  | 必要. 將檔案上傳至的公司的控制代碼。  |
| `uploadParams` (必要. XML `uploadParams`檔案，指定上傳參數) | `jobName`  |  `xsd:string`  | 需要`jobName`或`jobHandle`。 上載作業的名稱。  |
| `uploadParams` (必要. XML `uploadParams`檔案，指定上傳參數) | `jobHandle`  |  `xsd:string`  | 需要`jobName`或`jobHandle`。 處理在先前請求中開始的上載作業。  |
| `uploadParams` (必要. XML `uploadParams`檔案，指定上傳參數) | `locale`  |  `xsd:string`  | 選填。本地化的語言和國家代碼。  |
| `uploadParams` (必要. XML `uploadParams`檔案，指定上傳參數) | `description`  |  `xsd:string`  | 選填。工作說明。  |
| `uploadParams` (必要. XML `uploadParams`檔案，指定上傳參數) | `destFolder`  |  `xsd:string`  | 選填。檔案名屬性前置詞的目標資料夾路徑，尤其是對於瀏覽器和其他可能不支援檔案名中完整路徑的客戶端。  |
| `uploadParams` (必要. XML `uploadParams`檔案，指定上傳參數) | `fileName`  |  `xsd:string`  | 選填。目標檔案的名稱。 覆寫filename屬性。 |
| `uploadParams` (必要. XML `uploadParams`檔案，指定上傳參數) | `endJob`  |  `xsd:boolean`  | 選填。預設為 false。 |
| `uploadParams` (必要. XML `uploadParams`檔案，指定上傳參數) | `uploadParams`  |  `types:UploadPostJob`  | 如果這是現有活動作業的後續請求，則為可選。 如果存在現有作業，則會忽略`uploadParams`並使用現有作業上載參數。 請參閱[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

在`<uploadPostParams>`塊中是`<uploadParams>`塊，用於指定所包含檔案的處理。

請參閱[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)。

雖然您可能假設`uploadParams`參數會隨著同一工作的一部分而改變個別檔案，但情況並非如此。 對整個作業使用相同的`uploadParams`參數。

對新上載作業的初始POST請求應指定`jobName`參數，優選地使用唯一作業名稱來簡化後續作業狀態輪詢和作業日誌查詢。 對相同上載作業的其他POST請求應使用從初始請求返回的`jobHandle`值指定`jobHandle`參數，而非`jobName`。

上傳作業的最終POST請求應將`endJob`參數設為true，以便此作業不會對未來的檔案進行開機自檢。 接著，這可讓工作在所有POSTed檔案都收錄後立即完成。 否則，如果在30分鐘內未收到其他POST請求，則作業逾時。

## UploadPOST響應{#section-421df5cc04d44e23a464059aad86d64e}

對於成功的POST請求，響應主體將是XML `uploadPostReturn`文檔，如XSD在以下中所指定：

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

傳回的`jobHandle`會傳入`uploadPostParams`/ `jobHandle`參數，以用於相同工作的任何後續POST請求。 您也可以使用它來輪詢具有`getActiveJobs`操作的作業狀態，或使用`getJobLogDetails`操作查詢作業日誌。

如果處理POST請求時出錯，響應主體由[Faults](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)中所述的API故障類型之一組成。

## 範例POST請求{#section-810fe32abdb9426ba0fea488dffadd1e}

```
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## 範例POST回應——成功{#section-0d515ba14c454ed0b5196ac8d1bb156e}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## POST響應示例——錯誤{#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
