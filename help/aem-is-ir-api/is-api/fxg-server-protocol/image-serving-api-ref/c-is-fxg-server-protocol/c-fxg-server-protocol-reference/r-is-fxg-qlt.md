---
title: qlt
description: Jpeg品質。 指定JPEG編碼屬性來控制壓縮等級。 這進而會改變檔案大小（回覆資料量），並間接改變結果影像的視覺品質。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
TQID: 'https://experienceleague.adobe.com/sf3ydtf3lGCG1BfJfc1vW5hXFBawbeWJwXNSJdUEei8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 15%

---

# qlt{#qlt}

Jpeg品質。 指定JPEG編碼屬性來控制壓縮等級。 這進而會改變檔案大小（回覆資料量），並間接改變結果影像的視覺品質。

` qlt= *`品質`*[, *`色度`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">品質</span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG編碼品質(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">色度</span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度向下取樣（0=一般，1=停用）；選用，預設為0。 </p> </td> 
 </tr> 
</table>

僅在`fmt=jpg`時使用。 已忽略，否則

較高的值會增加檔案大小並提高品質，較低的值則會減少檔案大小並降低肉眼能感知的影像品質。 高於 90 的值所產生的影像通常與未壓縮的影像幾乎沒有差別。

設定`chroma`旗標以停用典型RGB編碼器所使用的JPEG色度縮減取樣。 當邊緣是由色相而非亮度的變化所定義時，這可能會增加影像中邊緣的感知銳利度。 設定此旗標可能會導致檔案大小稍微增加。 如果文字看起來有點模糊，請嘗試使用此設定。

如果輸出畫素型別為CMYK或灰色，則會忽略`chroma`。

## 範例 {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
