---
description: 請求和暈映修飾詞字串的查詢部分可能包含使用者定義的變數。
solution: Experience Manager
title: 自訂變數
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# 自訂變數{#custom-variables}

請求和暈映的查詢部分：：修飾詞字串可能包含使用者定義的變數。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **變數名稱。 可能包含字母、數字和安全字元的任意組合，但「$」除外。

** *[!DNL value]* **要設定變數的值（字串）。

變數的定義類似於其他伺服器命令，使用上述語法。 變數必須先定義，才能被參考。 在`vignette::Modifier`中定義的變數可在URL請求中參考，反之亦然。

>[!NOTE]
>
>*[!DNL value]* 必須是單次URL編碼，才能安全傳輸HTTP。如果&#x200B;*[!DNL value]*&#x200B;是透過HTTP重新傳輸，則需要雙重編碼。 當&#x200B;*[!DNL value]*&#x200B;被取代為巢狀外來請求時，即是如此。

變數的參考方式是將變數名稱（由前導和尾隨$括住）嵌入命令值中。 例如，在命令名稱后面的&#39;=&#39;和後續的&#39;&amp;&#39;或請求結尾之間。 伺服器將每次出現的$ *[!DNL name]*$替換為&#x200B;*[!DNL string]*。 在命令名稱中（在命令的等號之前）的$ *[!DNL name]*$的任何發生項以及請求的路徑部分中不會發生替代。

自訂變數不得巢狀化。 在&#x200B;*[!DNL string]*&#x200B;中，任何$ *[!DNL name]*$的出現次數都不會被取代。 例如，請求片段`$var2=apple&$var1=my$var2$tree&text=$var1$`解析為`text=my$var2$tree`。

$不是保留字元；在請求中可能會發生其他情況。 例如，`src=my$texture$file.tif`是有效命令（假設存在名為[!DNL my$texture$file.tif]的材料目錄條目或紋理檔案），而`wid=$number$`則否，因為`wid=`需要數字參數。
