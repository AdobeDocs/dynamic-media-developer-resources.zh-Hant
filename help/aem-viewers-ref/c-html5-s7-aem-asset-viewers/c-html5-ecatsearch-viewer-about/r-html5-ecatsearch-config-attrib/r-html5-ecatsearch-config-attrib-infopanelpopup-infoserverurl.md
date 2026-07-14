---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
TQID: 'https://experienceleague.adobe.com/en4zktUgJGVG-e0fahRGTxasP3CVxhgfie6d0e3q6r4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>資訊伺服器URL範本是用來擷取資訊面板內容範本中變數替代的索引鍵/值組。 指定的範本通常包含巨集預留位置，這些預留位置會在請求傳送至伺服器之前被實際資料取代。 </p> <p><span class="codeph"> $1$</span>已取代為觸發<span class="codeph"> InfoPanelPopup</span>啟用的變換值。 </p> <p><span class="codeph"> $2$</span>已取代為影像集中目前影格的序號。 </p> <p><span class="codeph"> $3$</span>已取代為目前專案之父集名稱中指定的第一個路徑元素。 通常會對應至目錄ID。 </p> <p><span class="codeph"> $4$</span>在路徑中取代為下列元素，並與資產ID相對應。 實際的資訊伺服器要求語法與資訊伺服器有關，而且會因伺服器而異。 例如，以下是典型的Dynamic Media資訊伺服器請求範本： </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>請注意，當您設定資訊面板快顯視窗時，傳遞給資訊面板的HTML程式碼和JavaScript程式碼會在使用者端電腦上執行。 因此，請確定這些HTML程式碼和JavaScript程式碼是安全的。

## 屬性 {#section-71356e3c13244e62b0582980d9d05328}

選擇性.

## 預設 {#section-22e9af803f724434807d34e200eb7518}

無。

## 範例 {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
