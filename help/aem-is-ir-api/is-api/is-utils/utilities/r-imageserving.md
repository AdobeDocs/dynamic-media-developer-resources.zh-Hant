---
description: 影像伺服控制指令碼。 此指令碼可用來啟動、停止或重新啟動「影像伺服伺服器監督程式」，接著啟動、停止或重新啟動所有其他的「影像伺服」元件。
solution: Experience Manager
title: imageserving
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
TQID: 'https://experienceleague.adobe.com/KyiS-GblbCE-Q4Exrdz8T1W5thFn9cHellB-1-QYZaw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 1%

---

# imageserving{#imageserving}

影像伺服控制指令碼。 此指令碼可用來啟動、停止或重新啟動「影像伺服伺服器監督程式」，接著啟動、停止或重新啟動所有其他的「影像伺服」元件。

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
   <td colname="col1"> <p> <span class="codeph">開始</span> </p> </td> 
   <td colname="col2"> <p> 啟動「伺服器管理員」和所有其他的「影像伺服」元件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">停止</span> </p> </td> 
   <td colname="col2"> <p> 停止所有「影像伺服」元件，包括「伺服器監督員」。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">重新啟動</span> </p> </td> 
   <td colname="col2"> <p>重新啟動所有「影像伺服」元件，包括「伺服器監督員」。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">重新啟動{ ps |是 | svg } </span> </p> </td> 
   <td colname="col2"> <p> 重新啟動Tomcat/[!DNL Platform Server]、影像伺服器或SVG。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">狀態[ ps |是 | svg ] </span> </p> </td> 
   <td colname="col2"> <p>傳回Image Server、Tomcat/[!DNL Platform Server]和SVGserver的運作時間與目前記憶體使用資訊，或只傳回指定伺服器的狀態；如果Server Supervisor未執行，則會傳回資訊訊息。 </p> </td> 
  </tr> 
 </tbody> 
</table>
