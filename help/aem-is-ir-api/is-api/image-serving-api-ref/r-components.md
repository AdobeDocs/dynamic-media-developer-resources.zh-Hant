---
description: '「場景7影像伺服」由下列元件組成 '
solution: Experience Manager
title: 影像提供元件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---

# 影像提供元件{#image-serving-components}

「場景7影像伺服」由下列元件組成：

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
   <td colname="col2"> <p>獨立執行檔，負責啟動、停止和確保其他元件的健全性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>為大部分的Java元件提供環境。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監控/警報服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 提供伺服器監控和電子郵件警報。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>平台伺服器 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理客戶端連接、日誌記錄、與其他元件的通信。 在<span class="filepath"> /is/image</span>處進行HTTP存取。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>快取服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理Platform Server的資料快取。 在/is/cache處進行HTTP存取。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>影像伺服器 </p> </td> 
   <td colname="col2"> <p>執行所有影像處理和影像檔案I/O操作。 32位和64位執行檔都適用於Linux（32位僅適用於Windows）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE文本渲染元件 </p> </td> 
   <td colname="col2"> <p>運行<span class="codeph"> textPs=</span>操作時，文本呈現服務的一個或多個實例可能處於活動狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG呈現元件 </p> </td> 
   <td colname="col2"> <p>獨立Java應用程式（不由Tomcat托管）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media影像轉譯(亦稱為。 演算伺服器) </p> </td> 
   <td colname="col2"> <p>需要個別的授權才能啟動。 在<span class="filepath"> /ir/render</span>處訪問HTTP。 所有影像呈現功能都整合到平台伺服器和影像伺服器中，沒有單獨的可執行元件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

預設目錄([!DNL default.ini])或特定影像目錄（有關詳細資訊，請參閱[影像目錄](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)）提供了其他配置設定。
