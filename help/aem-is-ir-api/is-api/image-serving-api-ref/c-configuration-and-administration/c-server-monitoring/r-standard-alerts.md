---
description: 標準警報在配置的平均間隔結束時與合併的電子郵件消息一起發送。
solution: Experience Manager
title: 標準警報
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 1%

---


# 標準警報{#standard-alerts}

標準警報在配置的平均間隔結束時與合併的電子郵件消息一起發送。

下表說明了各種標準警報類型。

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>警報類型</b> </th> 
   <th class="entry"> <b>標題ID</b> </th> 
   <th class="entry"> <b>說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>鎖定的請求 </p> </td> 
   <td> <p>鎖定 </p> </td> 
   <td> <p>當請求無法在指定臨界值內傳回回應給用戶端時傳送。 可以指示掛起請求，這可能導致Java線程池耗盡。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>高並行性 </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> 當並行處理的請求數(<i>overlap</i>)超過指定的閾值時發出。 可表示伺服器過載狀況。 </td> 
  </tr> 
  <tr> 
   <td> <p>最低流量 </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>當整體請求率低於指定臨界值時產生。 通常指出伺服器通訊問題（例如當伺服器離線時）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>錯誤率 </p> </td> 
   <td> <p>錯誤 </p> </td> 
   <td> <p>當取樣間隔內HTTP錯誤回應的平均速率超過指定的臨界值時發出。 可指示配置問題、遺失影像、網站程式設計或資料庫錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>回應時間 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>當取樣間隔期間的平均請求處理時間增加到超過指定臨界值時傳送。 通常表示伺服器或後端映像儲存系統的臨時或持續過載狀況。 </p> <p>計算平均回應時間時，不會考慮錯誤回應。 </p> </td> 
  </tr> 
 </tbody> 
</table>

