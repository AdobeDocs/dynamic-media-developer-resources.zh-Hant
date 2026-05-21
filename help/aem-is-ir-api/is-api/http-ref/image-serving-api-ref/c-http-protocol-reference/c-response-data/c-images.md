---
description: 如果要求成功完成，且要求不包含req=命令或req=img或req=tmb，則會傳回影像資料。
solution: Experience Manager
title: 影像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
TQID: 'https://experienceleague.adobe.com/1tStTbuCLrOG8XrPgOw5qH-VujpHXX8Pt0IWXg9329Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 1%

---

# 影像{#images}

如果要求成功完成，且要求不包含req=命令或req=img或req=tmb，則會傳回影像資料。

HTTP回應MIME型別是由`fmt=`所決定，或者，如果未指定`fmt=`，則是`<image/jpeg>`。

如果要求方法是無條件的`GET`或`HEAD`，則HTTP回應狀態為「200 OK」。

伺服器可能會以狀態&#39;304&#39; （未修改）回覆，且不會傳回任何影像資料以回應條件式`GET`要求（包含有效的`If-Modified-Since`或`If-None-Match`標頭）。
