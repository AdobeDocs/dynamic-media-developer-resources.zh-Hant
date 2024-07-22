---
title: 自訂變數
description: 請求的查詢部分以及暈映修飾元字串可能包含使用者定義的變數。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# 自訂變數{#custom-variables}

請求和暈映：：修飾元字串的查詢部分可能包含使用者定義的變數。

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` — 變數名稱。 可由任何字母、數字和安全字元的組合組成，不包括`$`。

`[!DNL value]` — 要設定變數的值（字串）。

變數的定義與其他伺服器命令類似，使用上述語法。 必須先定義變數，才能加以參照。 在`vignette::Modifier`中定義的變數可以在URL要求中參照，反之亦然。

>[!NOTE]
>
>`[!DNL value]`必須為單次URL編碼，才能安全HTTP傳輸。 若透過HTTP重新傳輸`[!DNL value]`，則需要雙重編碼。 此情況是將`[!DNL value]`替代成巢狀外部要求的情況。

將變數名稱（以前置字元和尾端`$`括住）內嵌在命令值中的任何位置來參考變數。 例如，在命令名稱后面的`=`和後續的`&`或要求的結尾之間。 伺服器會以`[!DNL string]`取代每個出現的`$ [!DNL name]$`。 命令名稱（在命令的等號之前）和要求的路徑部分中`$ [!DNL name]$`的任何事件都不會發生替代。

自訂變數不可巢狀化。 在`[!DNL string]`中任何`$ [!DNL name]$`的相符專案都不會被取代。 例如，要求片段`$var2=apple&$var1=my$var2$tree&text=$var1$`解析為`text=my$var2$tree`。

`$`不是保留字元；它可能會發生在請求中的其他位置。 例如，`src=my$texture$file.tif`是有效的命令（假設存在名為`[!DNL my$texture$file.tif]`的材料目錄專案或紋理檔案），而`wid=$number$`則否，因為`wid=`需要數值引數。
