---
title: 範例
description: 此示例使用「影像服務」對對象進行著色，並在一組小格中的一個中應用包含自定義文本的貼片。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# 範例{#examples}

此示例使用「影像服務」對對象進行著色，並在一組小格中的一個中應用包含自定義文本的貼片。

IR變數用於標識視頻、徽標影像和自定義文本。

的 `vignette::Modifier` 指定記錄中的欄位 *模板* 在物料目錄的維涅特圖上 `myCat` 包含以下內容：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

所有使用的小圖都列在材料目錄的視圖圖中 `myCat`。

客戶端現在可以發出以下請求來檢索預設映像（使用模板開頭定義的變數）:

[!DNL `https://server/myCat/template`]

以下請求指定要呈現的某些內容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

有關影像服務的詳細資訊，請參閱影像服務文檔 `text=` 的子菜單。
