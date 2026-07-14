---
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f1491091-f109-4836-b7f1-ad0619b72dce
TQID: 'https://experienceleague.adobe.com/IYNuZDz6uNspQbYv4nqBn5bUFD6y5BwRwUkrNvLVoMM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 2%

---

# setContainerId{#setcontainerid}

eCatalog檢視器的JavaScript API參考。

[!DNL ` setContainerId( *`containerId`*)`]

設定檢視器插入其中的`DOM`容器（通常是`DIV`）的識別碼。 不需要在呼叫此方法時建立容器元素。 但是，執行`init()`時容器必須存在。 必須在`init()`之前呼叫它。

如果檢視器組態資訊與`config` JSON物件一起傳遞至建構函式，則此方法為選用。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}容器的</span> ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
