---
description: 影像伺服控制指令碼。 此指令碼用於啟動、停止或重新啟動映像伺服器主管，該主管隨後將啟動、停止或重新啟動所有其他映像伺服器元件。
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---

# ImageServing{#imageserving}

影像伺服控制指令碼。 此指令碼用於啟動、停止或重新啟動映像伺服器主管，該主管隨後將啟動、停止或重新啟動所有其他映像伺服器元件。

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
   <td colname="col2"> <p> 啟動「伺服器主管」和所有其他「映像服務」元件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 停止  </span> </p> </td> 
   <td colname="col2"> <p> 停止所有映像服務元件，包括伺服器主管。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新啟動 </span> </p> </td> 
   <td colname="col2"> <p>重新啟動所有映像服務元件，包括伺服器主管。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新啟動{ ps |為 | svg }  </span> </p> </td> 
   <td colname="col2"> <p> 重新啟動Tomcat/Platform伺服器、影像伺服器或SVG。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 狀態[ ps |為 | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>返回映像伺服器、Tomcat/Platform伺服器和SVGserver的正常運行時間和當前記憶體使用資訊，或僅返回指定伺服器的狀態；如果伺服器主管未運行，則返回資訊性消息。 </p> </td> 
  </tr> 
 </tbody> 
</table>
