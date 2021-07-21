---
description: 包含平台伺服器設定。
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# server.xml{#server-xml}

包含平台伺服器設定。

修改此XML檔案時，必須小心維護有效的XML語法，否則平台伺服器可能無法啟動。

要使更改生效，必須在編輯此檔案後重新啟動Platform Server。

下圖說明了可以在此檔案中更改的設定。 請參閱本檔案前面的對應章節，以了解這些設定的說明。 請注意，此圖表不是[!DNL server.xml]的完整表示。

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
