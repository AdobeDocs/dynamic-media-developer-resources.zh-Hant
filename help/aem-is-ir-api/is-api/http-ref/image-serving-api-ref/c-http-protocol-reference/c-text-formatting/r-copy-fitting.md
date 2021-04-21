---
description: textPs=建置專屬的複製調整演算法，自動調整字型大小，以最佳化方式填入文字區域，將底部的額外空間減至最少，同時避免溢位。
solution: Experience Manager
title: 複製調整
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---


# Copy-fitting{#copy-fitting}

textPs=建置專屬的複製調整演算法，自動調整字型大小，以最佳化方式填入文字區域，將底部的額外空間減至最少，同時避免溢位。

可以對整個文本層（逐段），甚至對單個文本跨度，共同啟用和控制複製調整。

使用`\fs`指定最小字型大小，使用`\copyfit`指定最大字型大小。 允許在相同的RTF字串中使用任意數量的範圍。 所有範圍的大小會依比例而異，以確保維持所需的字型大小比例。

`\copyfit` 被視為字元格式命令，並具有範圍規則，如 `\fs` 和 `\b`。

指定`\copyfit`的大小等於或小於使用`\fs`指定的大小，可禁用複製管接頭。

## 限制行數{#section-e5aee0f039e04842afc3d6884ed681ac}

除了指定字型大小範圍外，還可使用`\copyfitlines`或`\copyfitmaxlines`命令進一步控制複製符合演算法的行為，以限制演算法將產生的行數。 這兩個命令都接受行數參數或0，以不限制複製擬合區域中的行數。

`\copyfitlines` 允許文字在不符合指定行數時溢出至其他行。要複製的文字區段中的明確分行一律採用。

`\copyfitmaxlines` 一律截斷超出指定限制的額外輸出行。即使存在明確的分行，也不會超出指定的行數。 在此版本的「影像伺服」中，複製符合的文字範圍中可能不超過N-1 `\line`標籤。 如果超過此限制，則行為未定義。

## 範例 {#section-f4ddbbfade444560be30a813d90c2c1b}

以下範例假設文字主體中提供名為&#x200B;*[!DNL $A$]*、*[!DNL $B$]*&#x200B;和&#x200B;*[!DNL $C$]*&#x200B;的變數。

**在整個範圍內，字型大小之間的比例保持相同：**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* 都會呈現兩倍於其餘文字的大小。當指定大量文字時，*[!DNL $A$]*&#x200B;和&#x200B;*[!DNL $C$]*&#x200B;將以`\fs10`和&#x200B;*[!DNL $B$]*&#x200B;以`\fs20`呈現。 對於小文本，*[!DNL $A$]*&#x200B;和&#x200B;*[!DNL $C$]*&#x200B;將使用`\fs100`和&#x200B;*[!DNL $B$]* `\fs200`。

**如果只繪製少量文字，則會收斂到一般的大字型大小：**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

在範圍的最小端，*[!DNL $B$]*&#x200B;將以`\fs20`呈現，其大小是&#x200B;*[!DNL $A$]*&#x200B;和&#x200B;*[!DNL $C$]*&#x200B;的2倍於`\fs10`。 所有文本都將在範圍的相反端`\fs100`（50分）繪製。

**如果要轉譯大量文字，請收斂至一般的小字型大小：**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

所有文本都在範圍的小端上以\fs10繪製，而最大的文本則以`\fs100`和&#x200B;*[!DNL $B$]*&#x200B;和`\fs200`顯示。*[!DNL $A$]**[!DNL $C$]*

**禁用內部文本範圍的複製調整：**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

*[!DNL $A$]*&#x200B;和&#x200B;*[!DNL $C$]*&#x200B;的字型大小在10到100之間不同，而&#x200B;*[!DNL $B$]*&#x200B;則一律以`\fs50`呈現。

**將輸出限制為單行（即使有更多垂直空間），但如果指定太多文字以適合單行，則允許輸出溢出至其他行(位於 `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**將輸出限制為單行，即使有更多垂直空間。如果指定的文字過多，而無法放入`\fs10`的單行中，則會截斷：**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
