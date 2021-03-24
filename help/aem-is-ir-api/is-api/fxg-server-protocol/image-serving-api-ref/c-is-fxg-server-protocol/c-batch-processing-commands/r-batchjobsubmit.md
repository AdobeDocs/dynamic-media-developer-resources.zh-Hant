---
description: 提交新批作業。
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 2%

---


# batchjobsubmit{#batchjobsubmit}

提交新批作業。

此參數：

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 作業資料  </span> </p> </td> 
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

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
