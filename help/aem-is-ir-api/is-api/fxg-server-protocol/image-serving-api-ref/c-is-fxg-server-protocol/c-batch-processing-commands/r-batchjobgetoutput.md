---
description: 檢索已提交作業的輸出。
seo-description: 檢索已提交作業的輸出。
seo-title: batchjobgetoutput
solution: Experience Manager
title: batchjobgetoutput
topic: Scene7 Image Serving - Image Rendering API
uuid: c2d49cc2-3223-4f0f-8ba7-4f74a5f76789
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# batchjobgetoutput{#batchjobgetoutput}

檢索已提交作業的輸出。

此參數：

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>提交時取得的工作ID。 </p> </td> 
 </tr> 
</table>

退貨：

作品的PDF輸出會以串流方式回應；錯誤： `jobid`無效或作業已刪除。

## 範例 {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
