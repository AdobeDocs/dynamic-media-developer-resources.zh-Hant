---
description: 提交新批作業。
seo-description: 提交新批作業。
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
topic: Scene7 Image Serving - Image Rendering API
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobsubmit{#batchjobsubmit}

提交新批作業。

此參數：

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 作業資料 </span> </p> </td> 
  <td class="stentry"> <p>完整工作資料的XML片段。 </p> </td> 
 </tr> 
</table>

退貨：

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>作業狀態 </p> </td> 
  <td class="stentry"> <p>提交是成功還是失敗；如果成功，作業ID將採用XML格式。 </p> </td> 
 </tr> 
</table>

## 範例 {#section-3886e8352e26419c97b24df21ca7f6fd}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&amp;jobdata=<URLEncodedXMLFileContents>]
