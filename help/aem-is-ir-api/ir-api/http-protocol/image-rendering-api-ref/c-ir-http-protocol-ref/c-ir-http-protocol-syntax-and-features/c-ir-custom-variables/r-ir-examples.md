---
description: 此範例使用「影像伺服」來為物件上色，並套用包含自訂文字的貼文(decal)至一組暈映。
solution: Experience Manager
title: 範例
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---


# 範例{#examples}

此範例使用「影像伺服」來為物件上色，並套用包含自訂文字的貼文(decal)至一組暈映。

IR變數可用來識別暈映、標誌影像和自訂文字。

材料目錄`myCat`暈映映射中名為&#x200B;*template*&#x200B;的記錄中的`vignette::Modifier`欄位包含以下內容：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

將使用的所有暈映都列在材料目錄`myCat`的暈映圖中。

用戶端現在可以提出下列要求來擷取預設影像（這會使用範本開頭所定義的變數）:

[!DNL `https://server/myCat/template`]

下列請求會指定要演算的特定內容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

有關「影像伺服`text=`」命令的詳細資訊，請參閱影像伺服檔案。
