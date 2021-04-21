---
description: 包含平台伺服器設定。
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# server.xml{#server-xml}

包含平台伺服器設定。

修改此XML檔案時，請務必保留有效的XML語法，否則平台伺服器可能無法啟動。

要使更改生效，必須在編輯此檔案後重新啟動平台伺服器。

下圖說明在此檔案中可更改哪些設定。 請參閱本文稍早的相應章節，以取得這些設定的說明。 請注意，此圖表不是[!DNL server.xml]的完整表示。

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```

