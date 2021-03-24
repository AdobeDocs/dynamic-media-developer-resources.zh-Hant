---
description: 輸出色彩描述檔。
solution: Experience Manager
title: icc
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---


# icc{#icc}

輸出色彩描述檔。

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 描述檔</span></span> </p></td> 
  <td class="stentry"> <p>ICC色彩描述檔。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent  </span> </span> </p></td> 
  <td class="stentry"> <p>知覺 |相對 |飽和度 |絕對| </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1要啟用，0要禁用黑點補償。 </p></td> 
 </tr> 
</table>

*`profile`* 指定輸出色域描述檔（如果轉換後的影像與工作描述檔不同）。*`profile`* 必須是在影像目 `icc::Name` 錄或預設目錄的ICC描述檔映射中定義的有效路徑，或是描述檔檔案的相對路徑(通常 [!DNL .icc]含或 [!DNL .icm] 尾碼)。

>[!NOTE]
>
>*`profile`* 不能包含&#39;,&#39;字元，即使HTTP編碼亦然。

*`renderIntent`* 允許覆蓋預設渲染方式。

*`blackpointComp`* 如果輸出配置檔案支援此功能，則啟用黑點補償。

>[!NOTE]
>
>並非所有色彩轉換都支援所有&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;選項。 通常，僅當ICC輸出配置檔案具有打印機或顯示器等輸出設備的特徵時，才執行這些設定。 此外，某些ICC輸出配置檔案不支援所有&#x200B;*`renderIntent`*&#x200B;選項。

## 屬性 {#section-b4042623a8ea40248c11b2153e5906b1}

可能發生在請求內的任何位置。 如果指定的影像類型`fmt=`不符合&#x200B;*`profile`*，則會傳回錯誤。

*`renderIntent`* 和 *`blackpointComp`* 如果與指定的ICC配置檔案不相容，則忽略。

CMYK輸出裝置描述檔更可能支援不同的轉換方式。

## 預設 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

如果已啟用色彩管理且未指定`icc=`，伺服器會傳送轉換為與`fmt=`指定之影像類型相符之輸出描述檔(`attribute::IccProfile*`)的影像。

如果未指定，則&#x200B;*`renderIntent`*&#x200B;繼承自`attribute::IccRenderIntent`,*`blackpointComp`*&#x200B;繼承自`attribute::IccBlackPointCompensation`。

## 另請參閱 {#section-37ef83149fd74345956a98f633cc0294}

[色彩管理](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)，屬 [性Profile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [Icc Embed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), icc: [, ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) [](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40) [icc屬性：:Icc RenderIntentIntent，屬性IccBlackPointCompensation:](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
