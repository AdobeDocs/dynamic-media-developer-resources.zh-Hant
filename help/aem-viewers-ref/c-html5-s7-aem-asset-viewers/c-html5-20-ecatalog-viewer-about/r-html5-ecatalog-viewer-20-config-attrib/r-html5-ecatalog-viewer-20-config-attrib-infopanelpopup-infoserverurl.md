---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>資訊伺服器URL範本可用來擷取資訊面板內容範本中變數替代的索引鍵/值組。指定的模板通常包含宏放置器，這些宏放置器在將請求發送到伺服器之前被實際資料替換。 </p> <p><span class="codeph"> $1$</span> 會以觸發 <span class="codeph"> InfoPanelPopup</span> 啟動。 </p> <p><span class="codeph"> $2$</span> 會以影像集中當前幀的序列號替換。 </p> <p><span class="codeph"> $3$</span> 替換為在當前項目的父集名稱中指定的第一個路徑元素。 它通常對應至目錄ID。 </p> <p><span class="codeph"> 4美元</span> 會在路徑中以下列元素取代，並與資產id相對應。 實際的資訊伺服器請求語法與資訊伺服器相關，且不同於伺服器。 例如，以下是典型的Dynamic Media資訊伺服器請求範本： </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>當您設定「資訊面板彈出畫面」時，傳遞至「資訊面板」的HTML代碼和JavaScript代碼會在用戶端的電腦上執行。 因此，請確定這類HTML程式碼和JavaScript程式碼是安全的。

## 屬性 {#section-71356e3c13244e62b0582980d9d05328}

選填。

## 預設 {#section-22e9af803f724434807d34e200eb7518}

無。

## 範例 {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
