---
description: 將資產上傳至Scene7 Production System涉及一或多個HTTP POST請求，這些請求會設定工作以協調與已上傳檔案相關的所有記錄檔活動。
seo-description: 將資產上傳至Scene7 Production System涉及一或多個HTTP POST請求，這些請求會設定工作以協調與已上傳檔案相關的所有記錄檔活動。
seo-title: 透過HTTP POST上傳資產至UploadFile Servlet
solution: Experience Manager
title: 透過HTTP POST上傳資產至UploadFile Servlet
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: dac273f51703fd63f1d427fbb7713fcc79bfa2c4

---


# 透過HTTP POST上傳資產至UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

將資產上傳至Scene7 Production System涉及一或多個HTTP POST請求，這些請求會設定工作以協調與已上傳檔案相關的所有記錄檔活動。

使用下列URL存取UploadFile Servlet:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>上傳作業的所有POST請求都必須源自相同的IP位址。

**存取Scene7地區的URL**

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

## 上傳工作的工作流程 {#section-873625b9512f477c992f5cdd77267094}

上傳工作由一或多個HTTP POST組成，這些HTTP POST使用通用 `jobHandle` 方式將處理關聯至同一工作。 每個請求都 `multipart/form-data` 經過編碼，由下清單單部分組成：

>[!NOTE]
>
>上傳作業的所有POST請求都必須源自相同的IP位址。

| HTTP POST表單部分|說明||-|-||`auth`|必要。 XML authHeader檔案，指定驗證和用戶端資訊。 請參 **閱SOAP** 下的 [請求驗證](/help/aem-ips-api/c-wsdl-versions.md)。 |
|`file params` |  選擇性. 您可以包含一或多個檔案，以便隨每個POST請求上傳。 每個檔案部件都可以在Content-Disposition標題中包含檔案名參數，如果未指定參數，則該參數將用作IPS中的目 `uploadPostParams/fileName` 標檔案名。 |

| HTTP POST表單部分| uploadPostParams元素名稱|類型|說明||-|-|-|-||`uploadParams` (必要。 指定上 `uploadParams` 傳參數的XML檔案)| `companyHandle`|`xsd:string`|必要。 將檔案上傳至的公司的控制代碼。 |
|`uploadParams` (必要. 指定上 `uploadParams` 傳參數的XML檔案)|`jobName`|`xsd:string`|需要 `jobName` 或 `jobHandle` 要求。 上載作業的名稱。 |
|`uploadParams` (必要. 指定上 `uploadParams` 傳參數的XML檔案)|`jobHandle`|`xsd:string`|需要 `jobName` 或 `jobHandle` 要求。 處理在先前請求中開始的上載作業。 |
|`uploadParams` (必要. 指定上 `uploadParams` 傳參數的XML檔案)|`locale`|`xsd:string`|選用。 本地化的語言和國家代碼。 |
|`uploadParams` (必要. 指定上 `uploadParams` 傳參數的XML檔案)|`description`|`xsd:string`|選用。 工作說明。 |
|`uploadParams` (必要. 指定上 `uploadParams` 傳參數的XML檔案)|`destFolder`|`xsd:string`|選用。 檔案名屬性前置詞的目標資料夾路徑，尤其是對於瀏覽器和其他可能不支援檔案名中完整路徑的客戶端。 |
|`uploadParams` (必要. 指定上 `uploadParams` 傳參數的XML檔案)|`fileName`|`xsd:string`|選用。 目標檔案的名稱。 覆寫filename屬性。 |
|`uploadParams` (必要. 指定上 `uploadParams` 傳參數的XML檔案)|`endJob`|`xsd:boolean`|選用。 預設為 false。|
|`uploadParams` (必要. 指定上 `uploadParams` 載參數的XML文檔)|`uploadParams`|`types:UploadPostJob`|如果這是對現有活動作業的後續請求，則為可選。 如果存在現有作業，則 `uploadParams` 會忽略並使用現有作業上載參數。 請參 [閱UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

塊內 `<uploadPostParams>` 是指 `<uploadParams>` 定所包含檔案處理的塊。

請參 [閱UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)。

雖然您可能認為， `uploadParams` 參數可以隨著同一工作而變更個別檔案，但情況並非如此。 對整個作 `uploadParams` 業使用相同的參數。

對新上載作業的初始POST請求應指定該參數，優選地 `jobName` 使用唯一作業名稱來簡化後續作業狀態輪詢和作業日誌查詢。 對相同上傳工作的其他POST請求應使用從 `jobHandle` 初始請求傳回 `jobName`的值， `jobHandle` 指定參數而非參數。

上傳工作的最終POST請求應將參 `endJob` 數設為true，以便此作業不會對未來的檔案進行POST。 接著，這可讓工作在所有POSTed檔案都收錄後立即完成。 否則，如果在30分鐘內未收到其他POST請求，則作業超時。

## UploadPOST回應 {#section-421df5cc04d44e23a464059aad86d64e}

若為成功的POST請求，回應內文將是XML文 `uploadPostReturn` 件，如XSD所指定：

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

傳 `jobHandle` 回的內容會傳入 `uploadPostParams`/參數， `jobHandle` 以取得相同工作的任何後續POST請求。 您也可以使用它來輪詢作業狀態和 `getActiveJobs` 操作，或查詢作業日 `getJobLogDetails` 志。

如果處理POST請求時出錯，則響應主體由Faults中所述的API故障類型之 [一組成](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)。

## POST請求範例 {#section-810fe32abdb9426ba0fea488dffadd1e}

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

## POST回應範例——成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## POST響應示例——錯誤 {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

