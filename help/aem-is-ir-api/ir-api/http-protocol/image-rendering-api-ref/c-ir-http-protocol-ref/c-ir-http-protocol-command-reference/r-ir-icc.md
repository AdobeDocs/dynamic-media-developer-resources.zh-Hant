---
title: icc
description: 輸出色彩設定檔。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
TQID: 'https://experienceleague.adobe.com/vC889xf6GmyiSls7qG81NPIegfh6OMZM2zMc4JKppAU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 1%

---

# icc{#icc}

輸出色彩設定檔。

icc= *`profile`*[， *`renderIntent`*[，*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">設定檔</span></span> </p></td> 
  <td class="stentry"> <p>ICC色彩設定檔。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>可感知 |相對 |飽和度 |絕對 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1代表啟用，0代表停用黑點補償。 </p></td> 
 </tr> 
</table>

*`profile`*&#x200B;如果演算後的影像與正在處理的設定檔不同，請指定應該轉換的輸出色域設定檔。*`profile`* 必須是定義於影像目錄或預設目錄之ICC設定檔對映中的有效`icc::Name`，或是設定檔檔案的相對路徑（通常具有[!DNL `.icc`]或[!DNL `.icm`]尾碼）。

>[!NOTE]
>
>*`profile`*&#x200B;不能包含&#39;，&#39;字元，即使HTTP編碼亦然。

*`renderIntent`*&#x200B;允許覆寫預設演算色彩比對方式。

*`blackpointComp`*&#x200B;如果輸出設定檔支援此功能，則啟用黑點補償。

>[!NOTE]
>
>並非所有的色彩轉換都支援所有&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;選擇。 通常，這些設定僅在ICC輸出設定檔為輸出裝置（例如印表機或顯示器）的特性時採用。 此外，有些ICC輸出設定檔不支援所有&#x200B;*`renderIntent`*&#x200B;選項。

## 屬性 {#section-b4042623a8ea40248c11b2153e5906b1}

可能發生在請求中的任何位置。 如果以`fmt=`指定的影像型別不符合&#x200B;*`profile`*，則傳回錯誤。

如果與指定的ICC設定檔不相容，則會同時忽略&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*。

CMYK輸出裝置設定檔較有可能支援不同的演算意圖。

## 預設 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

如果已啟用色彩管理且未指定`icc=`，則伺服器會將轉換的影像傳送至與`fmt=`所指定之影像型別相符的輸出設定檔( `attribute::IccProfile*`)。

如果未指定，*`renderIntent`*&#x200B;繼承自`attribute::IccRenderIntent`，而&#x200B;*`blackpointComp`*&#x200B;繼承自`attribute::IccBlackPointCompensation`。

## 另請參閱 {#section-37ef83149fd74345956a98f633cc0294}

[色彩管理](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)，[屬性：：IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)，[iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)，[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)，[屬性：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，[屬性：：IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)

