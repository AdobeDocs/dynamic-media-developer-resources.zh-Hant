---
description: 對於高級應用，可以將渲染操作的結果用作材料影像，就像從影像伺服中獲得的影像一樣。
solution: Experience Manager
title: 巢狀影像呈現請求
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# 巢狀影像呈現請求{#nested-image-rendering-requests}

對於高級應用，可以將渲染操作的結果用作材料影像，就像從影像伺服中獲得的影像一樣。

演算請求可在`src=`命令中指定，以作為材料影像，如下所示：

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir`代號區分大小寫。

巢狀請求不得包含影像呈現根路徑（通常為`http:// *[!DNL server]*/ir/render/'`），但可能包含預先處理規則代號。

在巢狀請求中指定下列命令時（在請求URL中或`catalog::Modifier`或`catalog::PostModifier`中）會遭到忽略：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

套用至巢狀轉譯請求的材料目錄的`attribute::MaxPix`和`attribute::DefaultPix`也會遭到忽略。

可選擇性地通過包括`cache=on`來快取嵌套IR請求的影像結果。 預設會停用中繼資料的快取。 只有當中間映像預期在合理的時間段內在不同請求中重複使用時，才應啟用快取。 標準伺服器端快取管理適用。 資料以無損格式快取。
