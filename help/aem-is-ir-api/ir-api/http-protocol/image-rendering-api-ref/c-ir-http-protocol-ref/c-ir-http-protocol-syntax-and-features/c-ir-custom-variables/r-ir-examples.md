---
description: 此範例使用「影像伺服」來為物件上色，並套用包含自訂文字的貼文(decal)至一組暈映。
seo-description: 此範例使用「影像伺服」來為物件上色，並套用包含自訂文字的貼文(decal)至一組暈映。
seo-title: 範例
solution: Experience Manager
title: 範例
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# 範例{#examples}

此範例使用「影像伺服」來為物件上色，並套用包含自訂文字的貼文(decal)至一組暈映。

IR變數可用來識別暈映、標誌影像和自訂文字。

物 `vignette::Modifier` 料目錄暈映圖 *中* ，記錄中名為template的欄位 `myCat` 包含以下內容：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

將使用的所有暈映都會列在材質目錄的暈映地圖中 `myCat`。

用戶端現在可以提出下列要求來擷取預設影像（這會使用範本開頭所定義的變數）:

[!DNL `https://server/myCat/template`]

下列請求會指定要演算的特定內容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

請參閱影像伺服檔案以取得影像伺服命令的詳細 `text=` 資訊。
