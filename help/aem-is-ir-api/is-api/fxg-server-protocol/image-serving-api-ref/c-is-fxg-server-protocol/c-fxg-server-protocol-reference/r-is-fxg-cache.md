---
description: 快取控制。 允許選擇性地停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）和內部 [!DNL Platform Server] 快取中的快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
TQID: 'https://experienceleague.adobe.com/X6q0OKRjjjpgNxl8XDuzkNBzrzTBS4E5BtXQGuJWgmk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 0%

---

# 快取{#cache}

快取控制。 允許選擇性地停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）和內部[!DNL Platform Server]快取中的快取。

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">開啟|關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">開啟|關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">開啟|關閉</span> </p></td> 
 </tr> 
</table>

如果只指定一個&#x200B;*`cacheControl`*&#x200B;值，則會同時套用至使用者端和伺服器快取。

要求屬性。 當要求未傳回回覆影像時忽略。 當影像目錄停用使用者端快取時（如果`catalog::Expiration`具有負值），會忽略&#x200B;*`clientControl`*。

預設為`cache=on,on`。
