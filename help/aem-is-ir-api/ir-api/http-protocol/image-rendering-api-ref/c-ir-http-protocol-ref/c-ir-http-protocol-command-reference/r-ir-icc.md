---
title: icc
description: 輸出顏色配置檔案。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# icc{#icc}

輸出顏色配置檔案。

icc= *`profile`*[, *`renderIntent`*[。*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 輪廓</span></span> </p></td> 
  <td class="stentry"> <p>ICC顏色配置檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 呈現意圖 </span> </span> </p></td> 
  <td class="stentry"> <p>知覺 |相對 |飽和度 |絕對 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 黑點元件</span> </span> </p></td> 
  <td class="stentry"> <p>1要啟用，0要禁用黑點補償。 </p></td> 
 </tr> 
</table>

*`profile`* 指定如果渲染影像與工作配置檔案不同，則應將其轉換為的輸出顏色空間配置檔案。 *`profile`* 必須是有效的 `icc::Name` 在映像目錄或預設目錄的ICC配置檔案映射中定義，或在配置檔案的相對路徑中定義(通常與 [!DNL `.icc`] 或 [!DNL `.icm`] 尾碼)。

>[!NOTE]
>
>*`profile`* 不能包含「，」字元，即使是HTTP編碼。

*`renderIntent`* 允許覆蓋預設渲染意圖。

*`blackpointComp`* 如果輸出配置檔案支援此功能，則啟用黑點補償。

>[!NOTE]
>
>並非所有顏色轉換都支援所有 *`renderIntent`* 和 *`blackpointComp`* 選項。 通常，僅當ICC輸出配置檔案表示輸出設備（如打印機或顯示器）時，才執行這些設定。 此外，某些ICC輸出配置檔案不支援所有 *`renderIntent`* 選項。

## 屬性 {#section-b4042623a8ea40248c11b2153e5906b1}

請求中的任何位置都可能發生。 如果指定的映像類型為 `fmt=` 不匹配 *`profile`*。

兩者 *`renderIntent`* 和 *`blackpointComp`* 如果與指定的ICC配置檔案不相容，則忽略。

CMYK輸出設備配置檔案更可能支援不同的渲染方式。

## 預設 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

如果啟用了顏色管理，並 `icc=` 未指定，伺服器將傳送轉換為輸出配置檔案( `attribute::IccProfile*`)與指定的映像類型匹配 `fmt=`。

如果未指定， *`renderIntent`* 繼承自 `attribute::IccRenderIntent`, *`blackpointComp`* 繼承自 `attribute::IccBlackPointCompensation`。

## 另請參閱 {#section-37ef83149fd74345956a98f633cc0294}

[色彩管理](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)。 [屬性：:IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)。 [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)。 [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)。 [屬性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)。 [屬性：:IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
