---
description: 包含平台伺服器設定。
seo-description: 包含平台伺服器設定。
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# server.xml{#server-xml}

包含平台伺服器設定。

修改此XML檔案時，請務必保留有效的XML語法，否則平台伺服器可能無法啟動。

要使更改生效，必須在編輯此檔案後重新啟動平台伺服器。

下圖說明在此檔案中可更改哪些設定。 請參閱本文稍早的相應章節，以取得這些設定的說明。 請注意，此圖表並非完整的表示 [!DNL server.xml]。

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

