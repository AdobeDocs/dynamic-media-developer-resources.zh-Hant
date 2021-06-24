---
description: 所有組態檔都位於install_folder/conf中，且可用大部分的文字編輯器編輯。 可能需要重新啟動伺服器才能使更改生效。
solution: Experience Manager
title: 伺服器配置檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# 伺服器配置檔案{#server-configuration-files}

所有組態檔都位於install_folder/conf中，且可用大部分的文字編輯器編輯。 可能需要重新啟動伺服器才能使更改生效。

>[!NOTE]
>
>大多數伺服器配置檔案都包含本文檔中未說明的其他屬性和值。 這些屬性供內部伺服器使用，除非Dynamic Media技術支援特別指示，否則不得修改。

本檔案探討下列組態檔的設定：

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>組態檔</b> </th> 
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
   <td> <p>平台伺服器配置。 </p> </td> 
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
   <td> <p>映像伺服器配置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

本檔案稍後會更詳細地討論組態檔。
