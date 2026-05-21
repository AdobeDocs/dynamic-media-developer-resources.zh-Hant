---
description: 擷取已提交工作的輸出。
solution: Experience Manager
title: batchjobgetoutput
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fb48c39-b15a-45b7-9aca-ed33f9c46c93
TQID: 'https://experienceleague.adobe.com/NxpHJlKxPQZT5YilheQ-MR0YfYO685pscRk76T1aU0A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 56
ht-degree: 1%

---

# batchjobgetoutput{#batchjobgetoutput}

擷取已提交工作的輸出。

此引數：

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">工作ID </span> </p> </td> 
  <td class="stentry"> <p>提交時取得的作業ID。 </p> </td> 
 </tr> 
</table>

傳回：

為回應，將工作的PDF輸出資料流化；如果`jobid`無效或工作已刪除，則會發生錯誤。

## 範例 {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp？req=batchjobgetoutput&amp;jobid=1005907604914d8eb63126b98f7172n76a5]
