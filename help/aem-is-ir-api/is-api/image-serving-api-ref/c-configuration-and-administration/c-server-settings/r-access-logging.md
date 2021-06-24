---
description: 使用這些伺服器設定進行記錄存取。
solution: Experience Manager
title: 存取記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 4%

---

# 存取記錄{#access-logging}

使用這些伺服器設定進行記錄存取。

語法

## TC::directory — 日誌檔案資料夾 {#section-5d9e2168d4504bbe9868b7d6051c9d67}

Platform伺服器將日誌檔案寫入的資料夾。 這可以是絕對路徑或相對於&#x200B;*`install_folder`*&#x200B;的路徑。 預設值為&#x200B;[!DNL  *`install_folder`*/logs]。

>[!NOTE]
>
>更改此設定之前必須建立新資料夾。 如果安裝「映像服務」以在root以外的用戶帳戶下運行，請確保資料夾具有正確的讀/寫訪問權限。

## TC::maxDays — 保留日誌檔案的天數 {#section-45cbecffc5694c87b7d5c176a44a4885}

應保留日誌檔案的天數。 每天午夜都會建立新的記錄檔。 此時，伺服器將刪除日誌檔案資料夾中早於指定天數的所有檔案，包括由映像伺服器或呈現伺服器寫入的檔案。 預設為 10。

## TC::prefix — 訪問日誌檔案名 {#section-1003856323b844049632710a5a056aa7}

寫入訪問日誌資料的檔案的名稱前置詞。 日期和檔案尾碼([!DNL  *`yyyy`*-*`mm`*-*`dd`*.log])會附加至指定的字串。 訪問日誌檔案的名稱必須與跟蹤日誌檔案的名稱不同。 預設為 &quot; `access-`&quot;.

## TC::pattern — 訪問日誌模式 {#section-22775ea85cee444d8a7d7336a3b1feef}

指定Platform Server訪問日誌記錄的資料模式。 模式字串指定用其對應值替換的變數。 模式字串中的所有其他字元都以字面方式傳送到記錄。

若要使用快取熱身公用程式，必須使用空格作為欄位分隔符號。 Platform伺服器將欄位值中的所有空格和「%」字元分別替換為`%20`和`%25`。

支援下列模式變數：

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>模式</b> </th> 
   <th class="entry"> <b>說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>遠程IP地址。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>本機IP位址。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>排除HTTP標題的回應位元組計數，若為零則為「 」。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>排除HTTP標題的回應位元組計數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>請求處理時間（以毫秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>執行緒id（用於交叉參考除錯/錯誤記錄項目）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>日期和時間，格式為<span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>:<span class="varname"> mm </span>:<span class="varname"> ss </span>。 <span class="varname"> SSS偏 </span> 移  </span> </p> <p> （<span class="varname"> SSS </span>為毫秒，<span class="varname">偏移</span>為GMT時間偏移）;將響應發送到客戶端時捕獲時間值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>請求方法(<span class="codeph">GET</span>、<span class="codeph">POST</span>等)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>請求重疊（同時處理的請求數）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>接收此請求的本地埠。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>查詢字串(在前面加上「？」 如果存在)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>第一行請求（請求方法、URI、HTTP版本）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>與<span class="codeph"> %r </span>相同，但將有限的HTTP編碼應用到URI以避免日誌解析問題。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP回應狀態代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S  </span> </p> </td> 
   <td> <p>使用者工作階段ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>日期和時間，使用通用日誌格式。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>已驗證的遠程用戶（如果有），否則為「。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URI路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v  </span> </p> </td> 
   <td> <p>本地伺服器名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>請求處理時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r  </span> </p> </td> 
   <td> <p>平台伺服器快取密鑰（快取檔案資料夾/名稱）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>Platform伺服器快取管理關鍵字：<span class="codeph"> {重複使用 |已建立 |已更新 |遠程 | REMOTE_CREATED | REMOTE_UPDATED |遠程快取 |已驗證 |已忽略 |未定義} </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r  </span> </p> </td> 
   <td> <p>回應MIME類型。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>發生上下文轉發時的目標上下文。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r  </span> </p> </td> 
   <td> <p><span class="codeph">標籤</span>回應標題值（回應資料的MD5簽章）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{異常}r  </span> </p> </td> 
   <td> <p>錯誤訊息. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>從映像伺服器檢索快取條目或資料所花的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>請求剖析和影像目錄查閱所花費的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>指示此請求是否嘗試了目錄系統之外的任何基於路徑的訪問。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p>快取群集中傳送快取項或「 — 」的對等伺服器的IP地址（如果<span class="codeph"> CacheUse </span>不是<span class="codeph"> REMOTE_CREATED </span>或<span class="codeph"> REMOTE_UPDATED </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>錯誤類別： </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=無錯誤。 </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>在伺服器上找不到1=映像。 </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS協定使用錯誤或1以外的內容錯誤。 </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=其他伺服器錯誤。 </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=請求因臨時伺服器超載而被拒絕。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r  </span> </p> </td> 
   <td> <p><span class="codeph"> req= </span>的大寫值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r  </span> </p> </td> 
   <td> <p>請求的主目錄的根ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r  </span> </p> </td> 
   <td> <p>將資料寫入輸出流後，Platform Server傳送回應所花費的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{大小}r  </span> </p> </td> 
   <td> <p>與<span class="codeph"> %B </span>類似，但包含304（未修改）響應的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r  </span> </p> </td> 
   <td> <p>所有規則集轉換後的最終URL。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader  </span>}i  </span> </p> </td> 
   <td> <p>指定的HTTP要求標題的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>指定的HTTP響應標頭的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

預設為 `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
