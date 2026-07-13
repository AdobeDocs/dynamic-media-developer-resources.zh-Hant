---
title: 影像
description: 如果要求成功完成，且要求不包含req=命令，或如果req=有下列其中一個值img， debug，則會傳回影像資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
TQID: 'https://experienceleague.adobe.com/4wHyyXX0gxz9ojr5g5Puu5fBhKXo4hZDjyBuVTao3rQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 1%

---

# 影像{#images}

如果要求成功完成，且要求不包含req=命令，或如果req=有下列其中一個值，則會傳回影像資料： img、debug

HTTP回應MIME型別是由`fmt=`所決定，或者，如果未指定`fmt=`，則取決於`attribute::Format`的值。

如果要求方法是無條件的`GET`或`HEAD`，則HTTP回應狀態為「200 OK」。

伺服器可能會以狀態&#39;304&#39; （未修改）回覆，且不會傳回任何影像資料以回應條件式`GET`要求（在`request-header`中有[!DNL If-Modified-Since]欄位）。

