---
description: 輸出顏色配置檔案。
solution: Experience Manager
title: icc
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# icc{#icc}

輸出顏色配置檔案。

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 設定檔</span></span> </p></td> 
  <td class="stentry"> <p>ICC顏色配置檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent  </span> </span> </p></td> 
  <td class="stentry"> <p>知覺 |相對 |飽和度 |絕對 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1為啟用，0為禁用黑點補償。 </p></td> 
 </tr> 
</table>

*`profile`* 指定輸出顏色空間配置檔案，如果渲染的影像與工作配置檔案不同，則應將其轉換為該輸出顏色空間配置檔案。*`profile`* 必須是影像目 `icc::Name` 錄或預設目錄的ICC配置檔案映射中定義的有效路徑，或是配置檔案的相對路徑(通常帶 [!DNL .icc]有或 [!DNL .icm] 尾碼)。

>[!NOTE]
>
>*`profile`* 不得包含&#39;,&#39;字元，即使是HTTP編碼亦然。

*`renderIntent`* 允許覆寫預設的呈現方式。

*`blackpointComp`* 如果輸出配置檔案支援此功能，則啟用黑點補償。

>[!NOTE]
>
>並非所有顏色轉換都支援所有&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;選項。 通常，僅當ICC輸出配置檔案表徵輸出設備（如打印機或顯示器）時，才執行這些設定。 此外，某些ICC輸出配置檔案不支援所有&#x200B;*`renderIntent`*&#x200B;選項。

## 屬性 {#section-b4042623a8ea40248c11b2153e5906b1}

可能發生在要求內的任何位置。 如果以`fmt=`指定的影像類型與&#x200B;*`profile`*&#x200B;不匹配，則返回錯誤。

*`renderIntent`* 如果 *`blackpointComp`* 與指定的ICC配置檔案不相容，則忽略和。

CMYK輸出設備配置檔案更可能支援不同的渲染意圖。

## 預設 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

如果啟用顏色管理且未指定`icc=`，則伺服器將傳送轉換為與`fmt=`指定的影像類型匹配的輸出配置檔案(`attribute::IccProfile*`)的影像。

如果未指定，則&#x200B;*`renderIntent`*&#x200B;繼承自`attribute::IccRenderIntent`，而&#x200B;*`blackpointComp`*&#x200B;繼承自`attribute::IccBlackPointCompensation`。

## 另請參閱 {#section-37ef83149fd74345956a98f633cc0294}

[顏色管理](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [屬性：:IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [屬性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [屬性：:IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
