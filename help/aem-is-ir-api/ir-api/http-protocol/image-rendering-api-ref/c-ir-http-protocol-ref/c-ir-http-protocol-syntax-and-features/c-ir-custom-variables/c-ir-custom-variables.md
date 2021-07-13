---
description: 請求和暈映修飾詞字串的查詢部分可能包括用戶定義的變數。
solution: Experience Manager
title: 自訂變數
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# 自訂變數{#custom-variables}

要求和變數的查詢部分：：修飾詞字串可能包含使用者定義的變數。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **變數名稱。 可由字母、數字和安全字元的任何組合組成，但「$」除外。

** *[!DNL value]* **要設定變數的值（字串）。

變數的定義類似於其他伺服器命令，使用上述語法。 必須先定義變數，才可供參考。 在`vignette::Modifier`中定義的變數可在URL要求中參照，反之亦然。

>[!NOTE]
>
>*[!DNL value]* 必須採用單通URL編碼，才能安全HTTP傳輸。如果透過HTTP重新傳輸&#x200B;*[!DNL value]*，則需要雙重編碼。 *[!DNL value]*&#x200B;取代為巢狀外部請求時即是如此。

在命令值中嵌入變數名稱（由前導和尾隨$括住）即可引用變數。 例如，在命令名稱后面的「=」與後續的「&amp;」或請求的結尾之間。 伺服器將$ *[!DNL name]*$的每次此類事件替換為&#x200B;*[!DNL string]*。 命令名稱中$ *[!DNL name]*$的任何出現次數（在命令的等號之前）以及請求的路徑部分中不會發生替代。

自訂變數不可巢狀。 *[!DNL string]*&#x200B;內$ *[!DNL name]*$的任何出現次數均未取代。 例如，要求片段`$var2=apple&$var1=my$var2$tree&text=$var1$`解析為`text=my$var2$tree`。

$不是保留字元；若非如此，則可能發生在要求中。 例如，`src=my$texture$file.tif`是有效命令（假設存在名為[!DNL my$texture$file.tif]的材料目錄條目或紋理檔案），而`wid=$number$`則否，因為`wid=`需要數字參數。
