---
description: 刪除作業的輸出。
seo-description: 刪除作業的輸出。
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
topic: Scene7 Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobdelete{#batchjobdelete}

刪除作業的輸出。

如果作業當前正在運行，則會立即停止該作業，並刪除其所有處理資訊。 如果作業成功完成，則其輸出檔案將被刪除。

此參數：

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>提交時取得的工作ID。 </p></td> 
 </tr> 
</table>

退貨：

在收到刪除請求時的作業狀態，如果無效或作業 `jobid` 已刪除，則出錯。

## 範例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
