---
description: 映像服務控制指令碼。 此指令碼用於啟動、停止或重新啟動映像服務伺服器管理器，然後啟動、停止或重新啟動所有其他映像服務元件。
solution: Experience Manager
title: 影像服務
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# 影像服務{#imageserving}

映像服務控制指令碼。 此指令碼用於啟動、停止或重新啟動映像服務伺服器管理器，然後啟動、停止或重新啟動所有其他映像服務元件。

## 使用 {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`命令`*`

## 命令 {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>命令 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 開始 </span> </p> </td> 
   <td colname="col2"> <p> 啟動伺服器主管和所有其他映像服務元件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 停止 </span> </p> </td> 
   <td colname="col2"> <p> 停止所有映像服務元件，包括伺服器主管。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新啟動 </span> </p> </td> 
   <td colname="col2"> <p>重新啟動所有映像服務元件，包括伺服器主管。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新啟動{ ps} | | svg } </span> </p> </td> 
   <td colname="col2"> <p> 重新啟動Tomcat/[!DNL Platform Server]、映像伺服器或SVG。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 狀態[ ps] | | svg ] </span> </p> </td> 
   <td colname="col2"> <p>返回Image Server、Tomcat/的正常運行時間和當前記憶體使用資訊[!DNL Platform Server]、和SVGserver，或僅指定伺服器的狀態；如果伺服器主管未運行，則返回一條資訊性消息。 </p> </td> 
  </tr> 
 </tbody> 
</table>
