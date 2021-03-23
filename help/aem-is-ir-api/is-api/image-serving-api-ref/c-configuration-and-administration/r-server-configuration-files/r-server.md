---
description: 包含平台伺服器設定。
seo-description: 包含平台伺服器設定。
seo-title: server.xml
solution: Experience Manager
title: server.xml
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員、商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
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

