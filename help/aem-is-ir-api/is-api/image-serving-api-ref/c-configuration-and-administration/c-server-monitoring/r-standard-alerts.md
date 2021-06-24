---
description: 在設定的平均間隔結束時，標準警報會與合併的電子郵件一起發送。
solution: Experience Manager
title: 標準警報
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 標準警報{#standard-alerts}

在設定的平均間隔結束時，標準警報會與合併的電子郵件一起發送。

下表說明了各種類型的標準警報。

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>警報類型</b> </th> 
   <th class="entry"> <b>標題Id</b> </th> 
   <th class="entry"> <b>說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>鎖定的請求 </p> </td> 
   <td> <p>鎖定 </p> </td> 
   <td> <p>當要求無法在指定的臨界值內傳回回應給用戶端時傳送。 可以指示掛起的請求，這可能導致Java線程池耗盡。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>高併發性 </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> 當同時處理的請求數(<i>overlap</i>)超過指定的臨界值時發出。 可能表示伺服器過載狀況。 </td> 
  </tr> 
  <tr> 
   <td> <p>最小流量 </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>當整體請求率低於指定的臨界值時產生。 通常表示伺服器通訊問題（例如當伺服器離線時）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>錯誤率 </p> </td> 
   <td> <p>錯誤 </p> </td> 
   <td> <p>當取樣間隔期間HTTP錯誤回應的平均速率超過指定的臨界值時發出。 可能表示配置問題、缺少影像、網站寫程式或資料庫錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>回應時間 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>當取樣間隔期間的平均請求處理時間增加到超過指定的臨界值時傳送。 通常表示伺服器或後端影像儲存系統的暫時或持續過載狀況。 </p> <p>計算平均回應時間時，不會考慮錯誤回應。 </p> </td> 
  </tr> 
 </tbody> 
</table>
