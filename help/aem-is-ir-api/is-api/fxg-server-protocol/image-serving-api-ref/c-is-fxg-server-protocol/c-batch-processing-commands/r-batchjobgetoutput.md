---
description: 擷取已提交工作的輸出。
solution: Experience Manager
title: batchjobgetoutput
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fb48c39-b15a-45b7-9aca-ed33f9c46c93
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '54'
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
