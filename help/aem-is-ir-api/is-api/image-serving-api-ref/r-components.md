---
title: 影像伺服元件
description: Dynamic Media影像伺服包含下列元件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---

# 影像伺服元件{#image-serving-components}

Dynamic Media影像伺服包含下列元件：

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>伺服器監督員 </p> </td> 
   <td colname="col2"> <p>獨立的可執行檔，負責啟動、停止及確保其他元件的健康狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>它為大部分的Java型元件提供環境。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監視/警示服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 提供伺服器監控和電子郵件警示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理使用者端連線、記錄、與其他元件的通訊。 位於<span class="filepath"> /is/image</span>的HTTP存取。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>快取服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理[!DNL Platform Server]的資料快取。 /is/cache上的HTTP存取。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>影像伺服器 </p> </td> 
   <td colname="col2"> <p>它會執行所有影像處理和影像檔案I/O作業。 32位元和64位元可執行檔都適用於Linux® （32位元僅適用於Windows）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE文字轉譯元件 </p> </td> 
   <td colname="col2"> <p>執行<span class="codeph"> textPs=</span>作業時，文字演算服務的一或多個執行個體可能作用中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG演算元件 </p> </td> 
   <td colname="col2"> <p>獨立式Java™應用程式（非由Tomcat託管）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media影像演算(亦稱為 演算伺服器) </p> </td> 
   <td colname="col2"> <p>它需要單獨的授權才能啟用。 位於<span class="filepath"> /ir/render</span>的HTTP存取。 所有影像演算功能已整合至[!DNL Platform Server]和影像伺服器，沒有個別的可執行元件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

預設目錄([!DNL default.ini])或特定影像目錄（如需詳細資訊，請參閱[影像目錄](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)）提供了其他組態設定。
