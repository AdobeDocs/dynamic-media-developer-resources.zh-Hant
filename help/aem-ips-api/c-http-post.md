---
title: 透過HTTP POST將資產上傳到UploadFile Servlet
description: 將資產上傳到 [!DNL Dynamic Media] 傳統版牽涉到一或多個HTTPPOST要求，這些要求會設定一個工作來協調與上傳檔案相關的所有記錄活動。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# 透過HTTP POST將資產上傳到UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

將資產上傳到Dynamic Media Classic涉及一個或多個HTTPPOST請求，這些請求會設定協調與上傳檔案關聯的所有記錄活動的工作。

使用下列URL存取UploadFile Servlet：

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>上載工作的所有POST請求都必須來自相同的IP位址。

**存取Dynamic Media地區的URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理位置 </p> </th> 
   <th colname="col2" class="entry"> <p>生產URL </p> </th> 
   <th colname="col3" class="entry"> <p>預備URL （用於生產前的開發和測試） </p> </th> 
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

## 上載工作的工作流程 {#section-873625b9512f477c992f5cdd77267094}

上載工作包含一或多個HTTP POST，這些HTTP POST使用通用`jobHandle`將處理關聯到相同工作。 每個請求都經過`multipart/form-data`編碼，由下清單單元件組成：

>[!NOTE]
>
>上載工作的所有POST請求都必須來自相同的IP位址。

|  HTTPPOST表單元件  |  說明  |
|---|---|
| `auth`  |   必填。 指定驗證和使用者端資訊的XML authHeader檔案。 請參閱[SOAP](/help/aem-ips-api/c-wsdl-versions.md)下的&#x200B;**要求驗證**。 |
| `file params`  |   選填。 您可以包含一或多個要隨著每個POST請求上傳的檔案。 每個檔案部分都可在Content-Disposition標頭中包含一個檔案名稱引數，如果未指定`uploadPostParams/fileName`引數，該引數將用作IPS中的目標檔案名稱。 |

|  HTTPPOST表單元件   |  uploadPostParams元素名稱   |  型別   |  說明   |
|---|---|---|---|
| `uploadParams` (必要。 XML `uploadParams`檔案指定上傳引數)   |   `companyHandle`  |  `xsd:string`  | 必填。 檔案上傳目標公司的控制代碼。  |
| `uploadParams` (必要。 XML `uploadParams`檔案指定上傳引數) | `jobName`  |  `xsd:string`  | 需要`jobName`或`jobHandle`。 上載工作的名稱。  |
| `uploadParams` (必要。 XML `uploadParams`檔案指定上傳引數) | `jobHandle`  |  `xsd:string`  | 需要`jobName`或`jobHandle`。 處理在先前請求中啟動的上傳工作。  |
| `uploadParams` (必要。 XML `uploadParams`檔案指定上傳引數) | `locale`  |  `xsd:string`  | 選填。 本地化的語言和國家/地區代碼。  |
| `uploadParams` (必要。 XML `uploadParams`檔案指定上傳引數) | `description`  |  `xsd:string`  | 選填。 工作的說明。  |
| `uploadParams` (必要。 XML `uploadParams`檔案指定上傳引數) | `destFolder`  |  `xsd:string`  | 選填。 檔案名稱屬性前置詞的目標資料夾路徑，特別是針對可能不支援檔案名稱完整路徑的瀏覽器和其他使用者端。  |
| `uploadParams` (必要。 XML `uploadParams`檔案指定上傳引數) | `fileName`  |  `xsd:string`  | 選填。 目標檔案的名稱。 覆寫檔案名稱屬性。 |
| `uploadParams` (必要。 XML `uploadParams`檔案指定上傳引數) | `endJob`  |  `xsd:boolean`  | 選填。 預設為 false。 |
| `uploadParams` (必要。 XML `uploadParams`檔案指定上傳引數) | `uploadParams`  |  `types:UploadPostJob`  | 如果這是針對現有作用中工作的後續請求，則為選用。 如果有現有工作，則會忽略`uploadParams`並使用現有工作上傳引數。 檢視[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

在`<uploadPostParams>`區塊中是指定處理所包含檔案的`<uploadParams>`區塊。

請參閱[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)。

雖然您可能會假設`uploadParams`引數可以隨著相同工作針對個別檔案變更，但情況並非如此。 在整個工作中使用相同的`uploadParams`引數。

新上傳工作的初始POST請求應指定`jobName`引數，最好使用唯一的工作名稱來簡化後續工作狀態輪詢和工作記錄查詢。 相同上載工作的其他POST要求應使用從初始要求傳回的`jobHandle`值，指定`jobHandle`引數，而非`jobName`。

上載工作的最終POST要求應該將`endJob`引數設定為true，如此此工作未來就不會對檔案進行POST。 反過來，這可讓工作在擷取所有POSTed檔案後立即完成。 否則，如果未在30分鐘內收到其他POST請求，則作業會逾時。

## uploadpost回應 {#section-421df5cc04d44e23a464059aad86d64e}

對於成功的POST要求，回應本文是XML `uploadPostReturn`檔案，如下列的XSD所指定：

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

針對相同工作的任何後續POST要求，傳回的`jobHandle`會傳入`uploadPostParams`/ `jobHandle`引數。 您也可以用它來輪詢具有`getActiveJobs`作業的工作狀態，或查詢具有`getJobLogDetails`作業的工作記錄檔。

如果處理POST要求時發生錯誤，回應主體會包含[錯誤](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)中說明的其中一個API錯誤型別。

## 範例POST請求 {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
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

```{.line-numbers}
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

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
