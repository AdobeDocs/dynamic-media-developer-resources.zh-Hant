---
description: 使用這些伺服器設定進行日誌訪問。
solution: Experience Manager
title: 存取記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 4%

---


# 訪問記錄{#access-logging}

使用這些伺服器設定進行日誌訪問。

語法

## TC::directory —— 日誌檔案資料夾{#section-5d9e2168d4504bbe9868b7d6051c9d67}

平台伺服器寫入日誌檔案的資料夾。 此路徑可以是相對於&#x200B;*`install_folder`*&#x200B;的絕對路徑或路徑。 預設值為&#x200B;[!DNL  *`install_folder`*/logs]。

>[!NOTE]
>
>必須先建立新資料夾，才能變更此設定。 如果安裝Image Serving以在root以外的用戶帳戶下運行，請確保資料夾具有正確的讀／寫訪問權限。

## TC::maxDays —— 保留日誌檔案的天數{#section-45cbecffc5694c87b7d5c176a44a4885}

應保留的日誌檔案的天數。 每天午夜都會建立新的記錄檔。 此時，伺服器將刪除日誌檔案資料夾中早於指定天數的所有檔案，包括由映像伺服器或渲染伺服器編寫的檔案。 預設為 10。

## TC::prefix —— 訪問日誌檔案名{#section-1003856323b844049632710a5a056aa7}

訪問日誌資料寫入到的檔案的名稱前置詞。 日期和檔案尾碼([!DNL  *`yyyy`*-*`mm`*-*`dd`*.log])附加到指定字串。 訪問日誌檔案的名稱必須與跟蹤日誌檔案的名稱不同。 預設為 &quot; `access-`&quot;.

## TC::pattern —— 訪問日誌模式{#section-22775ea85cee444d8a7d7336a3b1feef}

指定平台伺服器訪問日誌記錄的資料模式。 模式字串指定用其對應值取代的變數。 模式字串中的所有其他字元將字面傳輸到日誌記錄。

要使用快取預熱實用程式，必須使用空格作為欄位分隔符。 平台伺服器將欄位值中的所有空格和&#39;%&#39;字元分別替換為`%20`和`%25`。

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
   <td> <p>回應位元組計數排除HTTP標題，或「 」（如果為零）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>回應位元組計數，排除HTTP標題。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>請求處理時間（以毫秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>線程ID（用於交叉引用調試／錯誤日誌條目）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>日期和時間，格式為<span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>:<span class="varname"> mm </span>:<span class="varname"> ss </span>。 <span class="varname"> SSS偏 </span> 移  </span> </p> <p> （<span class="varname"> SSS </span>為毫秒，<span class="varname">偏移</span>為GMT時間偏移）;將回應傳送至用戶端時，會擷取時間值。 </p> </td> 
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
   <td> <p>收到此請求的本地埠。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>查詢字串（前置有'?'） 如果存在)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>第一行請求（request方法、URI、HTTP版本）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>與<span class="codeph"> %r </span>相同，但對URI應用有限的HTTP編碼以避免日誌解析問題。 </p> </td> 
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
   <td> <p>已驗證的遠程用戶（如果有），否則為「」。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URI路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v  </span> </p> </td> 
   <td> <p>本機伺服器名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>請求處理時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r  </span> </p> </td> 
   <td> <p>平台伺服器快取密鑰（快取檔案資料夾／名稱）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>平台伺服器快取管理關鍵字：<span class="codeph"> { REUSED |已建立 |已更新 |遠程 | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE |已驗證 |已忽略 | UNDEFINED } </span>。 </p> </td> 
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
   <td> <p><span class="codeph"> etag </span>回應標題值（回應資料的MD5簽名）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{例外}r  </span> </p> </td> 
   <td> <p>錯誤訊息. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>從Image Server擷取快取項目或資料所花的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>請求剖析和影像目錄查閱所花的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>指出此請求是否嘗試在目錄系統之外進行任何路徑型存取。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p>快取集群中傳送快取條目的對等伺服器的IP地址；如果<span class="codeph">快取使用</span>既不是<span class="codeph"> REMOTE_CREATED </span>也不是<span class="codeph"> REMOTE_UPDATED </span>，則為「-」。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>錯誤類別： </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=無錯誤。 </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=伺服器上未找到映像。 </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS通訊協定使用錯誤或1以外的內容錯誤。 </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=其他伺服器錯誤。 </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=因暫時伺服器過載而拒絕要求。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r  </span> </p> </td> 
   <td> <p>小寫值<span class="codeph"> req= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r  </span> </p> </td> 
   <td> <p>請求主目錄的根ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r  </span> </p> </td> 
   <td> <p>將資料寫入輸出串流後，Platform Server傳送回應所需的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{大小}r  </span> </p> </td> 
   <td> <p>類似<span class="codeph"> %B </span>，但包含304（未修改）回應的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r  </span> </p> </td> 
   <td> <p>所有規則集轉換後的最終URL。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader </span>}i  </span> </p> </td> 
   <td> <p>指定的HTTP請求標頭的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>指定HTTP回應標題的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

預設為 `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
