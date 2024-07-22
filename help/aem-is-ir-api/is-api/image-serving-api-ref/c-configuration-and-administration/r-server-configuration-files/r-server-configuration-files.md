---
title: 伺服器組態檔
description: 所有組態檔案都位於install_folder/conf中，並且可以用大多數文字編輯器進行編輯。 重新啟動伺服器讓變更生效。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# 伺服器組態檔{#server-configuration-files}

所有組態檔都在`install_folder/conf`中，且大多數的文字編輯器都可以編輯。 重新啟動伺服器讓變更生效。

>[!NOTE]
>
>大部分的伺服器組態檔都包含本檔案未說明的其他屬性和值。 這些屬性供內部伺服器使用，除非Dynamic Media技術支援人員指示，否則不得修改。

本檔案討論下列組態檔的設定：

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>組態檔</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>伺服器管理員組態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] 設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>目錄服務組態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>伺服器監視組態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>影像伺服器設定。 </p> </td> 
  </tr> 
 </tbody> 
</table>

本檔案稍後將更詳細地討論組態檔。
