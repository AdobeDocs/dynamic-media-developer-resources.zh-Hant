---
description: IPS Web服務受一組WSDL（Web服務描述語言）文檔的支援，這些文檔可從安裝了IPS Web服務元件的任何IPS安裝中訪問。 每個IPS API版本都包含引用版本控制目標XML命名空間的新WSDL檔案。 還支援以前的WSDL命名空間版本，以便向後相容現有應用程式。
solution: Experience Manager
title: IPS Web服務WSDL版本
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 1%

---

# IPS Web服務WSDL版本{#ips-web-service-wsdl-versions}

IPS Web服務受一組WSDL（Web服務描述語言）文檔的支援，這些文檔可從安裝了IPS Web服務元件的任何IPS安裝中訪問。 每個IPS API版本都包含引用版本控制目標XML命名空間的新WSDL檔案。 還支援以前的WSDL命名空間版本，以便向後相容現有應用程式。

## WSDL訪問 {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

訪問Scene7WSDL，如下所示。

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

預設值 `<IPS_webapp>` 是 `scene7`。

**服務位置**

服務URL在IPS Web服務WSDL文檔的服務部分中指定。 服務URL通常採用以下格式：

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

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
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>歐洲、中東、亞洲 </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本/亞太 </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## 支援的WSDL {#section-ebbba69880f94e9c823f1147974eb404}

請記住，如果要在最新版本的IPS API中使用功能，則可能需要修改代碼。 IPS API支援以下版本的WSDL:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API版本 </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API命名空間 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0之前 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

需要修改以使用新功能的現有應用程式必須升級到最新的API版本，並且可能需要更改現有代碼。 有關詳細資訊，請參閱更改日誌。

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**綁定**

IPS API Web服務僅支援SOAP綁定。

**支援的傳輸**

IPS API SOAP綁定僅支援HTTP傳輸。 使用HTTPSPOST方法生成所有SOAP請求。

**SOAP操作標頭**

要處理請求，請將SOAPAction HTTP標頭設定為請求操作的名稱。 WSDL綁定部分中的操作名稱屬性指定名稱。

**消息格式**

文檔/文字樣式用於所有輸入和輸出消息，其類型基於XML架構定義語言( [https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/))，並在WSDL檔案中指定。 所有類型都需要使用WSDL檔案中指定的目標命名空間值來限定名稱。

**請求驗證**

在API請求中傳遞驗證憑據的首選方法是使用 `authHeader` 元素，如IPS API WSDL中定義的。

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**Fields**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 使用者 </span> </p> </td> 
   <td colname="col2"> <p> 有效的IPS用戶電子郵件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 密碼 </span> </p> </td> 
   <td colname="col2"> <p>用戶帳戶的密碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 地區設定 </span> </p> </td> 
   <td colname="col2"> <p> 請求的可選區域設定。 請參閱 <b>區域設定</b> 的雙曲餘切值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> 正在調用應用程式名稱。 此參數是可選的，但建議將其包含在所有請求中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> 正在調用應用程式版本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzip響應 </span> </p> </td> 
   <td colname="col2"> <p> 用於啟用或禁用響應XML的gzip壓縮的可選標誌。 預設情況下，如果HTTP Accept-Encoding標頭表示支援gzip，則響應將被gzip壓縮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> 用於覆蓋故障響應的HTTP狀態代碼的可選參數。 預設情況下，故障響應返回HTTP狀態代碼500（內部伺服器錯誤）。 某些客戶端平台(包括AdobeFlash)無法讀取響應正文，除非返回狀態代碼200(OK)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

的 `authHeader` 元素始終在命名空間中定義 `http://www.scene7.com/IpsApi/xsd`，與API版本無關。

以下是使用 `authHeader` 請求SOAP標頭中的元素：

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**其他請求驗證方法**

如果由於某種原因，您的客戶端應用程式無法通過 `authHeader` SOAP頭、API請求也可以使用HTTP Basic身份驗證（如RFC 2617中所指定）指定憑據。

對於HTTP BasicPOST，每個SOAP驗證請求的HTTP標頭部分必須包含以下格式的標頭：

`Authorization: Basic base64(<IPS_user_email>:<password>)`

位置 `base64()` 應用標準Base64編碼， `<IPS_user_email>` 是有效IPS用戶的電子郵件地址， `<password>` 是用戶的密碼。

使用初始請求先發送授權標頭。 如果請求中未包含身份驗證憑據， `IpsApiService` 未以狀態代碼響應 `401 (Unauthorized)`。 相反，狀態代碼為 `500 (Internal Server Error)` 返回SOAP錯誤正文，指出無法驗證請求。

在IPS 3.8之前，通過SOAP頭進行身份驗證的方法是： `AuthUser` 和 `AuthPassword` 命名空間中的元素 `http://www.scene7.com/IpsApi`。 例如: 

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

此樣式仍支援向後相容，但已棄用 `authHeader` 的子菜單。

**請求授權**

在主叫方的憑據被認證後，檢查該請求以確保該主叫方被授權執行所請求的操作。 授權基於呼叫者的用戶角色，也可能需要檢查目標公司、目標用戶和其他操作參數。 此外，映像門戶用戶必須屬於具有執行某些資料夾和資產操作所需權限的組。 「操作參考」部分詳細說明了每個操作的授權要求。

**SOAP請求和響應示例**

以下示例顯示一個 `addCompany` 操作，包括HTTP標頭：

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

相應的反應是：

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**SOAP故障**

當操作遇到異常情況時，SOAP錯誤作為SOAP消息的正文返回，代替正常響應。 例如，如果非管理員用戶嘗試發送上一個 `addCompany` 請求，返回以下響應：

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```
