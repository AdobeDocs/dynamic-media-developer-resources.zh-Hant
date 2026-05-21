---
title: batchjobdelete
description: 刪除工作的輸出。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
TQID: 'https://experienceleague.adobe.com/1UB1BxMzt2kGisK6gosRfoI1LEilkLyHJvfP1AJbwwI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

刪除工作的輸出。

如果工作目前正在執行，則會立即停止，並刪除其所有處理資訊。 如果作業已成功完成，則會刪除其輸出檔案。

此引數：

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>提交時取得的作業ID。 </p></td> 
 </tr> 
</table>

傳回：

在收到刪除請求時的作業狀態，如果`jobid`無效或作業已被刪除時發生錯誤。

## 範例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
