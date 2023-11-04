---
description: 標準警報會在設定的平均間隔結束時，隨整合電子郵件訊息一起傳送。
solution: Experience Manager
title: 標準警報
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---

# 標準警報{#standard-alerts}

標準警報會在設定的平均間隔結束時，隨整合電子郵件訊息一起傳送。

下表說明每種標準警示型別。

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>警示型別</b> </th> 
   <th class="entry"> <b>標題ID</b> </th> 
   <th class="entry"> <b>說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>鎖定的請求 </p> </td> 
   <td> <p>鎖定 </p> </td> 
   <td> <p>當要求無法在指定的臨界值內傳回回應給使用者端時傳送。 可能表示有擱置要求，這會導致Java執行緒集區耗盡。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>高並行度 </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> 當同時處理的請求數時發出(當請求數 <i>重疊</i>)超過指定的臨界值。 可能表示伺服器超載情況。 </td> 
  </tr> 
  <tr> 
   <td> <p>最小流量 </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>當整體請求率低於指定臨界值時產生。 通常表示伺服器通訊問題（例如伺服器離線時）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>錯誤率 </p> </td> 
   <td> <p>錯誤 </p> </td> 
   <td> <p>在取樣間隔期間HTTP錯誤回應的平均速率超過指定臨界值時發出。 可能表示設定問題、影像遺失、網站程式設計或資料庫錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>回應時間 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>當取樣間隔期間的平均要求處理時間超過指定臨界值時傳送。 通常表示伺服器或後端影像儲存系統的暫時或持續超載情況。 </p> <p>計算平均回應時間時不考慮錯誤回應。 </p> </td> 
  </tr> 
 </tbody> 
</table>
