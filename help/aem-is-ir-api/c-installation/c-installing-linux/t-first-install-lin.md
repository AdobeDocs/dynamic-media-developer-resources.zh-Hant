---
description: 此過程說明如何在Linux上首次安裝Image Serving。
solution: Experience Manager
title: 首次安裝
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---


# 首次安裝{#installing-for-the-first-time}

此過程說明如何在Linux上首次安裝Image Serving。

1. 使用root權限登入您的伺服器主機。
1. 建立資料夾[!DNL /usr/local/scene7/licenses]。

   如果「影像伺服」和／或「影像演算」授權金鑰檔案（檔案尾碼為[!DNL .sc8]）可用，請將它複製到此資料夾。 否則，請繼續安裝，稍後再安裝授權金鑰。
1. 解壓縮並解壓縮Image Serving散發tar檔案。
1. 運行位於[!DNL Setup]資料夾中的[!DNL ./install-is]以啟動安裝嚮導。

   如果未找到許可證密鑰，將顯示說明如何獲取許可證檔案的說明。 此時請執行此操作，或繼續安裝映像服務，稍後安裝許可證密鑰。
1. 當顯示「使用者授權合約(EULA)」時，請閱讀授權合約，然後輸入`y`以繼續。

   安裝程式會顯示下表中所列的提示。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 主監聽埠[8080]:</span> </p> </td> 
   <td colname="col2"> <p>影像伺服和影像演算的主要HTTP監聽埠。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理員監聽埠[8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理員監聽埠。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 最大HTTP快取大小(MB)[2000]:</span> </p> </td> 
   <td colname="col2"> <p>主響應快取的初始大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 快取根資料夾[/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS快取資料夾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 影像伺服器擁有者ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>安裝映像伺服器的用戶帳戶。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 影像伺服器群組ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>要安裝映像伺服器的組帳戶。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 按&#x200B;**[!UICONTROL Enter]**&#x200B;接受預設值或指定不同的值。

   請確定指定的所有埠號都是唯一的，否則不會在此主機上使用。

   >[!IMPORTANT]
   >
   >如果指定了root以外的帳戶，則必須確保在配置檔案中重新配置這些資料夾時，正確設定了映像伺服器需要讀取和／或寫入的所有檔案和資料夾的訪問權限。
   >
   >映像服務現在已安裝到[!DNL /usr/local/Scene7/ImageServing]。 某些影像渲染內容安裝到[!DNL /usr/local/Scene7/ImageRendering]。
   >
   >在安裝接近尾聲時，安裝嚮導將嘗試啟動映像伺服器。 如果未找到有效的許可證密鑰，則無法啟動映像伺服器。 如果存在有效的許可證，但映像伺服器仍未啟動，請查閱日誌檔案。

>[!NOTE]
>
>如果許可證是在安裝映像服務後安裝的，則必須在使用之前手動啟動映像伺服器。
