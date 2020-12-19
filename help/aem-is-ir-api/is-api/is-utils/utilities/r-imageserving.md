---
description: 影像伺服控制指令碼。 此指令碼用於啟動、停止或重新啟動Image Serving Server Supervisor,Image Serving Server Supervisor又會啟動、停止或重新啟動所有其他Image Serving元件。
seo-description: 影像伺服控制指令碼。 此指令碼用於啟動、停止或重新啟動Image Serving Server Supervisor,Image Serving Server Supervisor又會啟動、停止或重新啟動所有其他Image Serving元件。
seo-title: ImageServing
solution: Experience Manager
title: ImageServing
topic: Scene7 Image Serving - Image Rendering API
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# ImageServing{#imageserving}

影像伺服控制指令碼。 此指令碼用於啟動、停止或重新啟動Image Serving Server Supervisor,Image Serving Server Supervisor又會啟動、停止或重新啟動所有其他Image Serving元件。

## 使用 {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`命令`*`

## 命令{#section-90436a0b0f70435f9ac42dafeed2c17b}

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
   <td colname="col2"> <p> 啟動Server Supervisor和所有其它Image Serving元件。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 重新啟動{ ps | is | svg }  </span> </p> </td> 
   <td colname="col2"> <p> 重新啟動Tomcat/Platform Server、Image Server或SVG。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 狀態[ ps | is | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>傳回影像伺服器、Tomcat/Platform伺服器和SVGserver的正常運作時間和目前記憶體使用資訊，或僅傳回指定伺服器的狀態；如果伺服器主管未運行，則返回資訊性消息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

