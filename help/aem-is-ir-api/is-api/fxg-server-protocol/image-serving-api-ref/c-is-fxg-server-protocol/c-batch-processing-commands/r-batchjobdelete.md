---
title: batchjobdelete
description: 刪除工作的輸出。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 3%

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

在收到刪除請求時的作業狀態，如果出現則為錯誤 `jobid` 無效或已刪除工作。

## 範例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
