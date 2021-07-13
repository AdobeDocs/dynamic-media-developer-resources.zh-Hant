---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>資訊伺服器URL範本可用來擷取資訊面板內容範本中變數替代的索引鍵/值組。指定的模板通常包含宏放置器，這些宏放置器在將請求發送到伺服器之前被實際資料替換。 </p> <p><span class="codeph"> $1$</span> 已取代為觸發InfoPanelPopupactivation的變換 <span class="codeph"> </span> 值。 </p> <p><span class="codeph"> $2$</span> 已替換為影像集中當前幀的序列號。 </p> <p><span class="codeph"> $3$</span> 已替換為在當前項的父集名稱中指定的第一個路徑元素。它通常對應至目錄ID。 </p> <p><span class="codeph"> $4$</span> 會在路徑中取代為下列元素，並與資產id對應。實際的資訊伺服器請求語法與資訊伺服器相關，且不同於伺服器。 例如，以下是典型的Dynamic Media資訊伺服器請求範本： </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>請注意，當您設定「資訊面板彈出畫面」時，傳遞至「資訊面板」的HTML程式碼和JavaScript程式碼會在用戶端的電腦上執行。 因此，請確定這類HTML程式碼和JavaScript程式碼是安全的。

## 屬性 {#section-71356e3c13244e62b0582980d9d05328}

選填。

## 預設 {#section-22e9af803f724434807d34e200eb7518}

無。

## 範例 {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
