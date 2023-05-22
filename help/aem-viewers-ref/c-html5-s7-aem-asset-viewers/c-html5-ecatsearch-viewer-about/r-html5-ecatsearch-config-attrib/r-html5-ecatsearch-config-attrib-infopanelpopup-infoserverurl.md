---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`資訊伺服器`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 資訊伺服器</span></span> </p> </td> 
   <td> <p>資訊伺服器URL模板用於在資訊面板內容模板中為變數替代提取密鑰/值對。 指定的模板通常包含宏佔位符，這些宏佔位符在請求發送到伺服器之前會替換為實際資料。 </p> <p><span class="codeph"> $1$</span> 替換為觸發 <span class="codeph"> 資訊面板彈出菜單</span> 激活。 </p> <p><span class="codeph"> $2$</span> 替換為影像集中當前幀的序列號。 </p> <p><span class="codeph"> $3$</span> 替換為在當前項目的父項集名稱中指定的第一個路徑元素。 它通常對應於目錄ID。 </p> <p><span class="codeph"> $4$</span> 替換為路徑中的以下元素，並與資產ID對應。 實際的資訊伺服器請求語法與資訊伺服器相關，不同於伺服器。 例如，以下是典型的Dynamic Media資訊伺服器請求模板： </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>請注意，配置「資訊面板」彈出菜單時，傳遞給「資訊面板」的HTML代碼和JavaScript代碼會在客戶端電腦上運行。 因此，請確保此類HTML代碼和JavaScript代碼是安全的。

## 屬性 {#section-71356e3c13244e62b0582980d9d05328}

選擇性.

## 預設 {#section-22e9af803f724434807d34e200eb7518}

無。

## 範例 {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
