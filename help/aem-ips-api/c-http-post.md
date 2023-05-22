---
title: 通過HTTP POST將資產上載到UploadFile Servlet
description: 將資產上載到 [!DNL Dynamic Media] 經典涉及一個或多個HTTPPOST請求，這些請求設定一個作業以協調與上載檔案關聯的所有日誌活動。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 3%

---

# 通過HTTP POST將資產上載到UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

將資產上載到Dynamic Media Classic涉及一個或多個HTTPPOST請求，這些請求設定一個作業以協調與上載檔案相關聯的所有日誌活動。

使用以下URL訪問UploadFile Servlet:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>上載作業的所有POST請求必須源於相同的IP地址。

**訪問Dynamic Media區域的URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理位置 </p> </th> 
   <th colname="col2" class="entry"> <p>生產URL </p> </th> 
   <th colname="col3" class="entry"> <p>暫存URL（用於預製開發和測試） </p> </th> 
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

## 上載作業的工作流 {#section-873625b9512f477c992f5cdd77267094}

上載作業由一個或多個使用公用HTTP POST的HTTP POST組成 `jobHandle` 將處理關聯到同一作業。 每個請求都 `multipart/form-data` 編碼，由以下窗體部件組成：

>[!NOTE]
>
>上載作業的所有POST請求必須源於相同的IP地址。

|  HTTPPOST窗體部件  |  說明  |
|---|---|
| `auth`  |   必要. 指定驗證和客戶端資訊的XML authHeader文檔。 請參閱 **請求驗證** 在 [SOAP](/help/aem-ips-api/c-wsdl-versions.md)。 |
| `file params`  |   選擇性. 您可以包括一個或多個要上載的檔案，其中包含每個POST請求。 每個檔案部件都可以在「內容處置」標題中包含檔案名參數，如果沒有，則該參數將用作IPS中的目標檔案名 `uploadPostParams/fileName` 指定參數。 |

|  HTTPPOST窗體部件   |  uploadPostParams元素名稱   |  類型   |  說明   |
|---|---|---|---|
| `uploadParams` (必要. XML `uploadParams` 指定上載參數的文檔)   |   `companyHandle`  |  `xsd:string`  | 必要. 對檔案上載到的公司的句柄。  |
| `uploadParams` (必要. XML `uploadParams` 指定上載參數的文檔) | `jobName`  |  `xsd:string`  | 要麼 `jobName` 或 `jobHandle` 。 上載作業的名稱。  |
| `uploadParams` (必要. XML `uploadParams` 指定上載參數的文檔) | `jobHandle`  |  `xsd:string`  | 要麼 `jobName` 或 `jobHandle` 。 在上一個請求中啟動的上載作業的句柄。  |
| `uploadParams` (必要. XML `uploadParams` 指定上載參數的文檔) | `locale`  |  `xsd:string`  | 選擇性. 本地化的語言和國家/地區代碼。  |
| `uploadParams` (必要. XML `uploadParams` 指定上載參數的文檔) | `description`  |  `xsd:string`  | 選擇性. 作業的說明。  |
| `uploadParams` (必要. XML `uploadParams` 指定上載參數的文檔) | `destFolder`  |  `xsd:string`  | 選擇性. 用於為filename屬性添加前置詞的目標資料夾路徑，特別是對於可能不支援檔案名中完整路徑的瀏覽器和其他客戶端。  |
| `uploadParams` (必要. XML `uploadParams` 指定上載參數的文檔) | `fileName`  |  `xsd:string`  | 選擇性. 目標檔案的名稱。 覆蓋filename屬性。 |
| `uploadParams` (必要. XML `uploadParams` 指定上載參數的文檔) | `endJob`  |  `xsd:boolean`  | 選擇性. 預設為 false。 |
| `uploadParams` (必要. XML `uploadParams` 指定上載參數的文檔) | `uploadParams`  |  `types:UploadPostJob`  | 如果這是現有活動作業的後續請求，則為可選。 如果有現有工作， `uploadParams` 忽略，並使用現有作業上載參數。 請參閱 [上載後作業](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

在 `<uploadPostParams>` 塊是 `<uploadParams>` 塊，用於指定所包含檔案的處理。

請參閱 [上載後作業](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)。

雖然你可能認為 `uploadParams` 參數可以作為同一作業的一部分更改單個檔案，但情況並非如此。 使用相同 `uploadParams` 整個作業的參數。

新上載作業的初始POST請求應指定 `jobName` 參數，最好使用唯一的作業名稱來簡化後續的作業狀態輪詢和作業日誌查詢。 同一上載作業的其他POST請求應指定 `jobHandle` 參數 `jobName`，使用 `jobHandle` 從初始請求返回的值。

上載作業的最終POST請求應設定 `endJob` 參數為true，以便此作業未對檔案進行開機自檢。 這又允許在接收所有POSTed檔案後立即完成作業。 否則，如果在30分鐘內未收到其他POST請求，則作業超時。

## UploadPOST響應 {#section-421df5cc04d44e23a464059aad86d64e}

對於成功的POST請求，響應體是XML `uploadPostReturn` 文檔，如XSD在下面中指定的：

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

的 `jobHandle` 返回時 `uploadPostParams`/ `jobHandle` 用於同一作業的任何後續POST請求的參數。 您也可以使用它輪詢作業狀態 `getActiveJobs` 或查詢作業日誌 `getJobLogDetails` 的下界。

如果處理POST請求時出錯，響應主體由API故障類型之一組成，如中所述 [故障](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)。

## 示例POST請求 {#section-810fe32abdb9426ba0fea488dffadd1e}

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

## 示例POST響應 — 成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## POST響應示例 — 錯誤 {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
