---
title: 自定義變數
description: 請求和可視修改量字串的查詢部分可以包括用戶定義的變數。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# 自定義變數{#custom-variables}

請求和vignette:：修改量字串的查詢部分可能包括用戶定義的變數。

`$ [!DNL name] = [!DNL value]`

`[!DNL name]`  — 變數名稱。 可能包含字母、數字和安全字元的任意組合，不包括 `$`。

`[!DNL value]`  — 要設定變數的值（字串）。

使用上述語法定義的變數與其他伺服器命令類似。 必須先定義變數，然後才能引用它們。 在中定義的變數 `vignette::Modifier` 可以在URL請求中引用，反之則可以。

>[!NOTE]
>
>`[!DNL value]` 必須是單通URL編碼，才能進行安全的HTTP傳輸。 如果需要雙重編碼， `[!DNL value]` 通過HTTP重傳。 這種情況下 `[!DNL value]` 替換為嵌套的外部請求。

通過嵌入變數名稱（由前導和尾隨圍成）來引用變數 `$`)命令值中的任意位置。 例如，在 `=`  按命令名和後續 `&` 或是請求的結束。 伺服器將每次此類事件 `$ [!DNL name]$` 與 `[!DNL string]`。 在任何 `$ [!DNL name]$` 在命令名稱（命令的等號之前）和請求的路徑部分中。

自定義變數可能不嵌套。 任何出現的 `$ [!DNL name]$` 內 `[!DNL string]` 的下界。 例如，請求片段 `$var2=apple&$var1=my$var2$tree&text=$var1$` 解析 `text=my$var2$tree`。

`$` 不是保留字元；在請求中可能會出現其它情況。 比如說， `src=my$texture$file.tif` 是有效命令(假定名為 `[!DNL my$texture$file.tif]` 存在)，而 `wid=$number$` 不是，因為 `wid=` 需要一個數字參數。
