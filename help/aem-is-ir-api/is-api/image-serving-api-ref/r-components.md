---
description: 場景7影像服務由以下元件組成
solution: Experience Manager
title: 影像服務元件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# 影像服務元件{#image-serving-components}

場景7影像服務由以下元件組成：

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>伺服器主管 </p> </td> 
   <td colname="col2"> <p>負責啟動、停止和確保其他元件運行狀況的獨立執行檔。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>為大多數基於Java的元件提供環境。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監視/警報服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 提供伺服器監控和電子郵件警報。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理客戶端連接、日誌記錄、與其他元件的通信。 HTTP訪問位於 <span class="filepath"> /is/image</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>快取服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理 [!DNL Platform Server]的資料快取。 位於/is/cache的HTTP訪問。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>影像伺服器 </p> </td> 
   <td colname="col2"> <p>執行所有影像處理和影像檔案I/O操作。 32位和64位執行檔都可用於Linux（僅適用於Windows的32位執行檔）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE文本呈現元件 </p> </td> 
   <td colname="col2"> <p>當文本呈現服務的一個或多個實例在 <span class="codeph"> textPs=</span> 運行操作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG渲染元件 </p> </td> 
   <td colname="col2"> <p>獨立的Java應用程式（不由Tomcat承載）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media影像渲染(亦稱。 演算伺服器) </p> </td> 
   <td colname="col2"> <p>需要單獨的許可證才能激活。 HTTP訪問位於 <span class="filepath"> /ir/render</span>。 所有影像渲染功能都整合到 [!DNL Platform Server] 和映像伺服器，沒有單獨的可執行元件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

預設目錄( [!DNL default.ini])或特定的映像目錄(請參見 [影像目錄](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) )。
