---
title: 範例
description: 此範例使用「影像伺服」將物件上色，並在一組暈映之一中套用包含自訂文字的貼花。
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

此範例使用「影像伺服」將物件上色，並在一組暈映之一中套用包含自訂文字的貼花。

IR變數可用來識別暈映、標誌影像和自訂文字。

材質目錄`myCat`的暈映對應中，名為&#x200B;*範本*&#x200B;之記錄中的`vignette::Modifier`欄位包含下列專案：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

所有使用的暈映都會列在材質目錄`myCat`的暈映對映中。

使用者端現在可以提出以下要求來擷取預設影像（使用在範本開頭定義的變數）：

[!DNL `https://server/myCat/template`]

以下請求指定要呈現的特定內容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

如需影像伺服`text=`命令的詳細資訊，請參閱影像伺服檔案。
