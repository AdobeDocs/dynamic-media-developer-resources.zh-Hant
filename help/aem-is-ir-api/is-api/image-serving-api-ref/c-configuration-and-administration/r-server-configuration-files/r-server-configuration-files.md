---
description: 所有配置檔案都位於install_folder/conf中，大多數文本編輯器都可編輯。 伺服器可能需要重新啟動才能使更改生效。
solution: Experience Manager
title: 伺服器配置檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 伺服器配置檔案{#server-configuration-files}

所有配置檔案都位於install_folder/conf中，大多數文本編輯器都可編輯。 伺服器可能需要重新啟動才能使更改生效。

>[!NOTE]
>
>大多數伺服器配置檔案包含本文檔中未說明的其他屬性和值。 這些屬性僅供內部伺服器使用，除非Dynamic Media技術支援部門特別指示，否則不得修改。

本文檔討論以下配置檔案的設定：

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>配置檔案</b> </th> 
   <th class="entry"> <b>說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>伺服器主管配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>平台伺服器組態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>目錄服務配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>伺服器監視配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>影像伺服器組態。 </p> </td> 
  </tr> 
 </tbody> 
</table>

本文稍後將更詳細地討論配置檔案。
