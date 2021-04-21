---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 2%

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>資訊伺服器URL範本可用來擷取資訊面板內容範本中變數替代的索引鍵／值配對。指定的範本通常包含巨集放置器，在將請求傳送至伺服器之前，巨集放置器會以實際資料取代。 </p> <p><span class="codeph"> $1$</span> 會以觸發InfoPanelPopupactivation的變換值 <span class="codeph"> </span> 取代。 </p> <p><span class="codeph"> $2$</span> 會以影像集中目前影格的序號取代。 </p> <p><span class="codeph"> $3$</span> 將替換為在當前項目的父項集名稱中指定的第一個路徑元素。它通常對應於目錄ID。 </p> <p><span class="codeph"> $4$</span> 會取代為路徑中的下列元素，並對應至資產ID。實際的資訊伺服器要求語法與資訊伺服器相關，並不同於伺服器。 例如，以下是典型的Dynamic Media資訊伺服器請求模板： </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>請注意，當您設定「資訊面板彈出畫面」時，傳送至「資訊面板」的HTML程式碼和JavaScript程式碼會在用戶端的電腦上執行。 因此，請確定此類HTML程式碼和JavaScript程式碼是安全的。

## 屬性 {#section-71356e3c13244e62b0582980d9d05328}

選填。

## 預設 {#section-22e9af803f724434807d34e200eb7518}

無。

## 範例 {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
