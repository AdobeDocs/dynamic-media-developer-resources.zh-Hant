---
description: 檢索已提交作業的詳細狀態。
seo-description: 檢索已提交作業的詳細狀態。
seo-title: batchjobdetailstatus
solution: Experience Manager
title: batchjobdetailstatus
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---


# batchjobdetailsstatus{#batchjobdetailedstatus}

檢索已提交作業的詳細狀態。

此參數：

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>提交時取得的工作ID。 </p> </td> 
 </tr> 
</table>

退貨：

XML格式作業的詳細狀態；錯誤： `jobid`無效或作業已刪除。

## 範例 {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
