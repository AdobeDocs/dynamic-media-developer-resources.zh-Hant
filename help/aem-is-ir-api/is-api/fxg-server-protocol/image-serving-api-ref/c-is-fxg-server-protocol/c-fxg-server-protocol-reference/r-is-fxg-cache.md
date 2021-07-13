---
description: 快取控制。 可選擇性地停用用戶端快取（瀏覽器、代理伺服器、網路快取系統）和內部Platform伺服器快取中的快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# 快取{#cache}

快取控制。 可選擇性地停用用戶端快取（瀏覽器、代理伺服器、網路快取系統）和內部Platform伺服器快取中的快取。

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 開啟/關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟/關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟/關閉</span> </p></td> 
 </tr> 
</table>

如果只指定了一個&#x200B;*`cacheControl`*&#x200B;值，則該值將同時應用於客戶端和伺服器快取。

要求屬性。 當要求未傳回回影像時忽略。 *`clientControl`* 當影像目錄停用用戶端快取時(如果 `catalog::Expiration` 有負值)，則會忽略。

預設為`cache=on,on`。
