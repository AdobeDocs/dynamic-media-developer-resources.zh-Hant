---
description: 將資產上傳至Dynamic Media Classic涉及一或多個HTTPPOST請求，這些請求會設定工作來協調與上傳之檔案相關聯的所有記錄活動。
solution: Experience Manager
title: 透過HTTP POST上傳資產至UploadFile Servlet
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: e7c747c44d27ed1769ab872d962a814d80c0b345
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 3%

---

# 透過HTTP POST上傳資產至UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

將資產上傳至Dynamic Media Classic涉及一或多個HTTPPOST請求，這些請求會設定工作來協調與上傳之檔案相關聯的所有記錄活動。

使用下列URL來存取UploadFile Servlet:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>上傳作業的所有POST請求都必須源自相同的IP位址。

**存取Dynamic Media地區的URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理位置 </p> </th> 
   <th colname="col2" class="entry"> <p>生產URL </p> </th> 
   <th colname="col3" class="entry"> <p>測試URL（用於生產前開發和測試） </p> </th> 
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
   <td colname="col1"> <p>日本/亞太 </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## 上傳工作的工作流程 {#section-873625b9512f477c992f5cdd77267094}

上傳作業包含一或多個使用通用`jobHandle`的HTTP POST，以將處理與相同作業產生關聯。 每個要求都經過`multipart/form-data`編碼，並由下清單單部分組成：

>[!NOTE]
>
>上傳作業的所有POST請求都必須源自相同的IP位址。

|  HTTPPOST表單部分  |  說明  |
|---|---|
| `auth`  |   必要. 指定驗證和客戶端資訊的XML authHeader文檔。 請參閱[SOAP](/help/aem-ips-api/c-wsdl-versions.md)下的&#x200B;**請求驗證**。 |
| `file params`  |   選擇性. 您可以包含一或多個要隨著每個POST請求上傳的檔案。 若未指定`uploadPostParams/fileName`參數，則每個檔案部件都可以在Content-Disposition標頭中包含檔案名參數，該參數用作IPS中的目標檔案名。 |

|  HTTPPOST表單部分   |  uploadPostParams元素名稱   |  類型   |  說明   |
|---|---|---|---|
| `uploadParams` (必要. 指定上載參數的XML `uploadParams`文檔)   |   `companyHandle`  |  `xsd:string`  | 必要. 處理要上傳檔案的公司。  |
| `uploadParams` (必要. 指定上載參數的XML `uploadParams`文檔) | `jobName`  |  `xsd:string`  | 需要`jobName`或`jobHandle`。 上傳作業的名稱。  |
| `uploadParams` (必要. 指定上載參數的XML `uploadParams`文檔) | `jobHandle`  |  `xsd:string`  | 需要`jobName`或`jobHandle`。 處理先前請求中開始的上傳作業。  |
| `uploadParams` (必要. 指定上載參數的XML `uploadParams`文檔) | `locale`  |  `xsd:string`  | 選填。本地化的語言和國家/地區代碼。  |
| `uploadParams` (必要. 指定上載參數的XML `uploadParams`文檔) | `description`  |  `xsd:string`  | 選填。工作說明。  |
| `uploadParams` (必要. 指定上載參數的XML `uploadParams`文檔) | `destFolder`  |  `xsd:string`  | 選填。指向檔案名屬性前置詞的目標資料夾路徑，尤其是對於可能不支援檔案名中完整路徑的瀏覽器和其他用戶端。  |
| `uploadParams` (必要. 指定上載參數的XML `uploadParams`文檔) | `fileName`  |  `xsd:string`  | 選填。目標檔案的名稱。 覆蓋檔案名屬性。 |
| `uploadParams` (必要. 指定上載參數的XML `uploadParams`文檔) | `endJob`  |  `xsd:boolean`  | 選填。預設為 false。 |
| `uploadParams` (必要. 指定上載參數的XML `uploadParams`文檔) | `uploadParams`  |  `types:UploadPostJob`  | 如果這是現有活動作業的後續請求，則為可選。 如果存在現有作業，則忽略`uploadParams`並使用現有作業上載參數。 請參閱[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

在`<uploadPostParams>`塊內是指定處理包含檔案的`<uploadParams>`塊。

請參閱[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)。

雖然您可以假設在同一作業中，個別檔案的`uploadParams`參數會有所變更，但情況並非如此。 在整個作業中使用相同的`uploadParams`參數。

新上傳作業的初始POST請求應指定`jobName`參數，最好使用唯一的作業名簡化後續作業狀態輪詢和作業日誌查詢。 對相同上傳作業的其他POST請求應使用從初始請求傳回的`jobHandle`值，指定`jobHandle`參數，而非`jobName`。

上傳作業的最終POST請求應將`endJob`參數設為true，以便此作業不會對任何未來檔案進行POST。 接著，這可讓工作在所有POSTed檔案都擷取完成後立即完成。 否則，若在30分鐘內未收到其他POST請求，則作業會逾時。

## UploadPOST回應 {#section-421df5cc04d44e23a464059aad86d64e}

對於成功的POST請求，響應正文將是XML `uploadPostReturn`文檔，如XSD中所指定：

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

傳回的`jobHandle`會傳入`uploadPostParams`/ `jobHandle`參數，以供後續POST相同作業的請求使用。 您也可以使用它輪詢`getActiveJobs`操作的作業狀態，或查詢`getJobLogDetails`操作的作業日誌。

如果處理POST請求時出錯，則響應正文由[Faults](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)中描述的API故障類型之一組成。

## 範例POST請求 {#section-810fe32abdb9426ba0fea488dffadd1e}

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

## 範例POST回應 — 成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## 範例POST回應 — 錯誤 {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
