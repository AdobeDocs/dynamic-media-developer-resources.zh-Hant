---
description: 'Scene 7 Image Serving包含下列元件 '
solution: Experience Manager
title: 影像伺服元件
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# 影像伺服元件{#image-serving-components}

Scene 7 Image Serving包含下列元件：

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
   <td colname="col2"> <p>負責啟動、停止和確保其他元件運行正常的獨立執行檔。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>為大多數基於Java的元件提供環境。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監控／警報服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 提供伺服器監控和電子郵件警報。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>平台伺服器 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理客戶端連接、日誌記錄和與其他元件的通信。 位於<span class="filepath"> /is/image</span>的HTTP存取。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>快取服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理平台伺服器的資料快取。 位於/is/cache的HTTP訪問。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>影像伺服器 </p> </td> 
   <td colname="col2"> <p>執行所有影像處理和影像檔案I/O操作。 32位元和64位元可執行檔都適用於Linux（僅適用於Windows的32位元）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE Text Render元件 </p> </td> 
   <td colname="col2"> <p>當運行<span class="codeph"> textPs=</span>操作時，文本渲染服務的一個或多個實例可以處於活動狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG Render元件 </p> </td> 
   <td colname="col2"> <p>可獨立執行的Java應用程式（非由Tomcat托管）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media影像演算(亦即。 演算伺服器) </p> </td> 
   <td colname="col2"> <p>需要個別的授權才能啟動。 位於<span class="filepath"> /ir/render</span>的HTTP訪問。 所有影像演算功能都整合在平台伺服器和影像伺服器中，而不需個別的可執行元件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

預設目錄([!DNL default.ini])或特定影像目錄（如需詳細資訊，請參閱[影像目錄](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)）提供其他組態設定。
