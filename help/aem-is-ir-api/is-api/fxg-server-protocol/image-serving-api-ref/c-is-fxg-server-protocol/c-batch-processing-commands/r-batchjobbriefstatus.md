---
description: 檢索已提交作業的匯總狀態。
seo-description: 檢索已提交作業的匯總狀態。
seo-title: batchobbriefstatus
solution: Experience Manager
title: batchobbriefstatus
uuid: 601e8395-8a77-4324-9cd7-5fe321bc91e3
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---


# batchjobbriefstatus{#batchjobbriefstatus}

檢索已提交作業的匯總狀態。

此參數：

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>提交時取得的工作ID。 </p> </td> 
 </tr> 
</table>

退貨：

XML格式的作業簡況；錯誤：jobid無效或作業已刪除。

## 範例 {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
