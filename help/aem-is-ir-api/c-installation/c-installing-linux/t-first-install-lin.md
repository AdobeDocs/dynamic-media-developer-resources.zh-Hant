---
title: 第一次安裝
description: 此程式說明如何在Linux®上首次安裝「影像伺服」。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# 第一次安裝{#installing-for-the-first-time}

此程式說明如何在Linux®上首次安裝「影像伺服」。

1. 以根許可權登入您的伺服器主機。
1. 建立資料夾[!DNL /usr/local/scene7/licenses]。

   如果「影像伺服」和/或「影像轉譯」授權金鑰檔案（含[!DNL .sc8]檔案字尾）可供使用，請將其複製到此資料夾。 否則，請繼續安裝並在稍後安裝授權金鑰。
1. 解壓縮並解壓縮「影像伺服」發佈tar檔案。
1. 在[!DNL Setup]資料夾中，執行[!DNL ./install-is]以啟動安裝精靈。

   如果找不到許可證金鑰，則會顯示說明如何取得許可證檔案的指示。 此時請執行此動作，或繼續安裝影像伺服，並於稍後安裝授權金鑰。
1. 當使用者授權合約(EULA)顯示時，請閱讀授權合約，然後輸入`y`以繼續。

   安裝程式會顯示下表中所列的提示。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">主要接聽連線埠[8080]：</span> </p> </td>
   <td colname="col2"> <p>影像提供與影像轉譯的主要HTTP接聽連線埠。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">管理員接聽連線埠[8083]：</span> </p> </td> 
   <td colname="col2"> <p>管理員接聽連線埠。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> HTTP快取大小上限(MB) [2000]：</span> </p> </td> 
   <td colname="col2"> <p>主要回應快取的初始大小。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph">快取根資料夾[/usr/local/scene7/ImageServing/cache]：</span> </p> </td> 
   <td colname="col2"> <p>PS快取資料夾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">影像伺服器擁有者識別碼[root]：</span> </p> </td>
   <td colname="col2"> <p>要安裝「影像伺服」伺服器的使用者帳戶。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph">影像伺服器群組識別碼[root]：</span> </p> </td>
   <td colname="col2"> <p>要安裝「影像伺服」伺服器的群組帳戶。 </p> </td>
  </tr>
 </tbody>
</table>

1. 按&#x200B;**[!UICONTROL Enter]**&#x200B;接受預設值或指定其他值。

   請確定所有指定的連線埠號碼都是唯一的，而且不會在此主機上使用。

   >[!IMPORTANT]
   >
   >如果指定了root以外的帳戶，則當在組態檔中重新設定這些資料夾時，您必須確定已正確設定影像伺服器需要讀取和寫入的所有檔案與資料夾的存取許可權。
   >
   >影像伺服現已安裝至[!DNL /usr/local/Scene7/ImageServing]。 某些影像演算內容已安裝到[!DNL /usr/local/Scene7/ImageRendering]。
   >
   >安裝結束時，安裝精靈會嘗試啟動Image Server。 如果找不到有效的授權金鑰，則無法啟動影像伺服器。 如果有有效的授權且Image Server尚未啟動，請查閱記錄檔。

>[!NOTE]
>
>如果在安裝「影像伺服」後安裝了授權，則必須手動啟動影像伺服器才能使用。
