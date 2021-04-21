---
description: IPS Web服務受一組WSDL（Web服務描述語言）文檔的支援，這些文檔可從安裝IPS Web服務元件的任何IPS安裝中訪問。 每個IPS API版本都包含參考版本化目標XML命名空間的新WSDL檔案。 也支援舊版WSDL命名空間版本，以便向後相容於現有的應用程式。
solution: Experience Manager
title: IPS Web服務WSDL版本
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 1%

---


# IPS Web服務WSDL版本{#ips-web-service-wsdl-versions}

IPS Web服務受一組WSDL（Web服務描述語言）文檔的支援，這些文檔可從安裝IPS Web服務元件的任何IPS安裝中訪問。 每個IPS API版本都包含參考版本化目標XML命名空間的新WSDL檔案。 也支援舊版WSDL命名空間版本，以便向後相容於現有的應用程式。

## WSDL訪問{#section-62e69fa2c87f4dc9bca72f10ba028f6c}

存取Scene7WSDL，如下所示。

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

`<IPS_webapp>`的預設值為`scene7`。

**服務位置**

服務URL在IPS Web服務WSDL文檔的服務部分中指定。 服務URL通常為：

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

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
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>歐洲、中東、亞洲 </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本／亞太地區 </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## 支援的WSDL {#section-ebbba69880f94e9c823f1147974eb404}

請記住，如果您想要使用最新版IPS API中的功能，可能需要修改代碼。 IPS API支援下列版本的WSDL:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API發行版本 </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API命名空間 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0之前版本 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

需要修改以使用新功能的現有應用程式必須升級至最新的API版本，而且可能需要變更現有的程式碼。 如需詳細資訊，請參閱變更記錄。

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**系結**

IPS API Web服務僅支援SOAP綁定。

**支援的傳輸**

IPS API SOAP綁定僅支援HTTP傳輸。 使用HTTPSPOST方法發出所有SOAP請求。

**SOAP操作標題**

若要處理請求，請將SOAPAction HTTP標題設為請求的作業名稱。 WSDL綁定部分中的操作名稱屬性指定名稱。

**消息格式**

文檔／常值樣式用於基於XML架構定義語言([http://www.w3.org/TR/xmlschema-0/](http://www.w3.org/TR/xmlschema-0/))並在WSDL檔案中指定的所有類型的輸入和輸出消息。 所有類型都需要使用WSDL檔案中指定的目標命名空間值來限定名稱。

**要求驗證**

在API請求中傳遞驗證憑證的偏好方法是使用IPS API WSDL中定義的`authHeader`元素。

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
   <td colname="col2"> <p>使用者帳戶的密碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 地區設定 </span> </p> </td> 
   <td colname="col2"> <p> 請求的選用地區設定。 如需詳細資訊，請參閱<b>地區設定</b>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName  </span> </p> </td> 
   <td colname="col2"> <p> 呼叫應用程式名稱。 此參數為選擇性，但建議您將其納入所有請求中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion  </span> </p> </td> 
   <td colname="col2"> <p> 呼叫應用程式版本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse  </span> </p> </td> 
   <td colname="col2"> <p> 可選標幟，可啟用或停用回應XML的gzip壓縮。 依預設，如果HTTP Accept-Encoding標題指出支援gzip，則回應會壓縮為gzip。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode  </span> </p> </td> 
   <td colname="col2"> <p> 可選參數，以覆寫錯誤回應的HTTP狀態程式碼。 預設情況下，故障響應返回HTTP狀態代碼500（內部伺服器錯誤）。 有些用戶端平台(包括AdobeFlash)無法讀取回應內文，除非傳回200（確定）的狀態碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

無論API版本為何，`authHeader`元素一律在namespace `http://www.scene7.com/IpsApi/xsd`中定義。

以下是在請求SOAP標題中使用`authHeader`元素的範例：

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

如果由於某些原因，您的客戶端應用程式無法傳遞`authHeader` SOAP標題，則API請求還可以使用HTTP Basic驗證（如RFC 2617中所指定）指定憑據。

對於HTTP基本驗證，每個SOAPPOST請求的HTTP標題區段必須包含表單標題：

`Authorization: Basic base64(<IPS_user_email>:<password>)`

其中`base64()`應用標準Base64編碼，`<IPS_user_email>`是有效IPS用戶的電子郵件地址，而`<password>`是用戶的密碼。

使用初始請求以搶先方式傳送授權標題。 如果請求中未包含驗證憑證，`IpsApiService`不會以`401 (Unauthorized)`的狀態碼回應。 相反地，會傳回`500 (Internal Server Error)`的狀態碼，並傳回SOAP錯誤內文，指出無法驗證請求。

在IPS 3.8之前，通過SOAP標頭的驗證是使用命名空間`http://www.scene7.com/IpsApi`中的`AuthUser`和`AuthPassword`元素實施的。 例如：

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

此樣式仍支援向後相容性，但已過時，傾向於`authHeader`元素。

**請求授權**

在對呼叫者的認證進行認證後，檢查請求以確保呼叫者被授權執行所請求的操作。 授權是基於呼叫者的用戶角色，而且可能需要檢查目標公司、目標用戶和其他操作參數。 此外，Image Portal使用者必須屬於具有執行特定資料夾和資產作業所需權限的群組。 「操作參考」部分詳細說明了每個操作的授權要求。

**範例SOAP要求與回應**

下列範例顯示完整的`addCompany`操作，包括HTTP標題：

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

而相應的回應是：

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

**SOAP錯誤**

當操作遇到異常條件時，SOAP錯誤作為SOAP消息的正文返回，以代替正常響應。 例如，如果非管理員使用者嘗試傳送先前的`addCompany`請求，則會傳回下列回應：

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

