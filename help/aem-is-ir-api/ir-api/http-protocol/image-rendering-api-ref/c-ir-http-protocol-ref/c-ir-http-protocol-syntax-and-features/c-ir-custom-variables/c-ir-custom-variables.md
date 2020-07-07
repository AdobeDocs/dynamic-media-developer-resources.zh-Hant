---
description: 請求和暈映修飾詞字串的查詢部分可能包含使用者定義的變數。
seo-description: 請求和暈映修飾詞字串的查詢部分可能包含使用者定義的變數。
seo-title: 自訂變數
solution: Experience Manager
title: 自訂變數
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Custom variables{#custom-variables}

請求和暈映的查詢部分：：修飾詞字串可能包含使用者定義的變數。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variable name. 可能包含字母、數字和安全字元的任意組合，但「$」除外。

** *[!DNL value]* **變數要設定的值（字串）。

變數的定義類似於其他伺服器命令，使用上述語法。 變數必須先定義，才能被參考。 在中定義的變 `vignette::Modifier` 數可在URL請求中參考，反之亦然。

>[!NOTE]
>
>*[!DNL value]* 必須是單次URL編碼，才能安全傳輸HTTP。 如果透過HTTP重新傳輸，則 *[!DNL value]* 需要雙重編碼。 在將其取代為巢 *[!DNL value]* 狀外來請求時，即是如此。

變數的參考方式是將變數名稱（由前導和尾隨$括住）嵌入命令值中。 例如，在命令名稱后面的&#39;=&#39;和後續的&#39;&amp;&#39;或請求結尾之間。 伺服器會以$ *[!DNL name]*$取代每次出現 *[!DNL string]*。 在命令名稱中（在命令的等號之前）和請求的路徑部分中，不會對任何$ *[!DNL name]*$的發生項進行替換。

自訂變數不得巢狀化。 在中發生的任何 *[!DNL name]*$$都 *[!DNL string]* 不會被取代。 例如，請求片段 `$var2=apple&$var1=my$var2$tree&text=$var1$` 解析為 `text=my$var2$tree`。

$不是保留字元； 在請求中可能會發生其他情況。 例如， `src=my$texture$file.tif` 是有效命令（假設名為材料目錄條目或紋理檔案存在），而 [!DNL my$texture$file.tif] 不是，因為 `wid=$number$``wid=` 需要數值參數。
