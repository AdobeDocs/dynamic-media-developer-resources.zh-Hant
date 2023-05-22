---
description: 使用這些伺服器設定進行日誌訪問。
solution: Experience Manager
title: 訪問日誌記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 3%

---

# 訪問日誌記錄{#access-logging}

使用這些伺服器設定進行日誌訪問。

語法

## TC::directory — 日誌檔案資料夾 {#section-5d9e2168d4504bbe9868b7d6051c9d67}

資料夾 [!DNL Platform Server] 寫入日誌檔案。 這可以是絕對路徑或相對於 *`install_folder`*。 預設值為 [!DNL  *`install_folder`*/日誌]。

>[!NOTE]
>
>必須先建立新資料夾，然後才能更改此設定。 如果安裝Image Serving以在除根用戶以外的用戶帳戶下運行，請確保資料夾具有正確的讀/寫訪問權限。

## TC::maxDays — 保留日誌檔案的天數 {#section-45cbecffc5694c87b7d5c176a44a4885}

應保留的日誌檔案天數。 每天午夜都會建立新日誌檔案。 此時，伺服器將刪除日誌檔案資料夾中早於指定天數的所有檔案，包括由映像伺服器或呈現伺服器編寫的檔案。 預設為 10。

## TC::prefix — 訪問日誌檔案名 {#section-1003856323b844049632710a5a056aa7}

寫入訪問日誌資料的檔案的名稱前置詞。 日期和檔案尾碼( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.日誌])。 訪問日誌檔案的名稱必須與跟蹤日誌檔案的名稱不同。 預設為 &quot; `access-`&quot;.

## TC::pattern — 訪問日誌模式 {#section-22775ea85cee444d8a7d7336a3b1feef}

指定的資料模式 [!DNL Platform Server] 訪問日誌記錄。 模式字串指定用其相應值替換的變數。 模式字串中的所有其他字元將字面地傳輸到日誌記錄。

要使用快取預熱實用程式，必須使用空格作為欄位分隔符。 的 [!DNL Platform Server] 將欄位值中的所有空格和「%」字元替換為 `%20` 和 `%25`的下界。

支援以下模式變數：

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
   <td> <p>本地IP地址。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>響應位元組計數（不包括HTTP標頭），或「 」（如果為零）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>響應位元組計數，不包括HTTP標頭。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>請求處理時間（毫秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>線程id（用於交叉引用調試/錯誤日誌條目）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %g </span> </p> </td> 
   <td> <p>日期和時間，格式為 <span class="codeph"> <span class="varname"> y </span>- <span class="varname"> 毫米 </span>- <span class="varname"> d </span> <span class="varname"> HH </span>: <span class="varname"> 毫米 </span>: <span class="varname"> ss </span>。 <span class="varname"> SSS </span> 偏移 </span> </p> <p> ( <span class="varname"> SSS </span> 是毫秒， <span class="varname"> 偏移 </span> 是GMT時間偏移);將響應發送到客戶端時捕獲時間值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>請求方法( <span class="codeph"> GET </span>。 <span class="codeph"> POST </span>等)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>請求重疊（同時處理的請求數）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>收到此請求的本地埠。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>查詢字串（以「？」為前置詞） )。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>第一行請求（請求方法、URI、HTTP版本）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>與 <span class="codeph"> %r </span>，但將有限的HTTP編碼應用於URI以避免日誌解析問題。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP響應狀態代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>用戶會話ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>日期和時間，以公用日誌格式。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>已驗證的遠程用戶（如果有），否則「」。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URI路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>本地伺服器名。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>請求處理時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] 快取密鑰（快取資料夾/名稱）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] 快取管理關鍵字： <span class="codeph"> {重複使用 |建立 |已更新 |遠程 |遠程建立 | REMOTE_UPDATED |遠程快取 |已驗證 |忽略 |未定義} </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>響應MIME類型。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{上下文}r </p> </td> 
   <td> <p>如果出現上下文轉發，則目標上下文。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{摘要}r </span> </p> </td> 
   <td> <p>的 <span class="codeph"> etag </span> 響應報頭值（響應資料的MD5簽名）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{異常}r </span> </p> </td> 
   <td> <p>錯誤訊息. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>從Image Server檢索快取條目或資料所花費的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>請求分析和影像目錄查找所花費的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>指示此請求是否嘗試了目錄系統之外的任何基於路徑的訪問。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>快取群集中傳遞快取項的對等伺服器的IP地址，如果 <span class="codeph"> 快取使用 </span> 都不是 <span class="codeph"> 遠程建立 </span> 無 <span class="codeph"> 遠程更新(_U) </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>錯誤類別： </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=無錯誤。 </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>在伺服器上找不到1=映像。 </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS協定使用錯誤或1以外的內容錯誤。 </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=其他伺服器錯誤。 </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=請求因臨時伺服器過載而被拒絕。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>上殼值 <span class="codeph"> 請求= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>請求主目錄的根ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>所花的時間 [!DNL Platform Server] 在將資料寫入輸出流後發送響應。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{大小}r </span> </p> </td> 
   <td> <p>像 <span class="codeph"> %B </span>，但包括304（未修改）響應的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>所有規則集轉換後的最終URL。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>} </span> </p> </td> 
   <td> <p>指定的HTTP請求標頭的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>指定的HTTP響應標頭的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

預設為 `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
