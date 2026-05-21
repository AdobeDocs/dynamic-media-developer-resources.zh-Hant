---
title: 巢狀影像演算請求
description: 對於進階應用程式，可以將轉譯作業的結果當做材質影像使用，就像從「影像伺服」取得的影像一樣。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
TQID: 'https://experienceleague.adobe.com/Fqiu-HsaRtrWMjBQudUBzr1iu3WLg7173Kf-71ikejI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# 巢狀影像演算請求{#nested-image-rendering-requests}

對於進階應用程式，可以將轉譯作業的結果當做材質影像使用，就像從「影像伺服」取得的影像一樣。

您可以在`src=`命令中指定轉譯要求，將它當做材質影像使用，如下所示：

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir`權杖區分大小寫。

巢狀要求不得包含影像演算根路徑（通常為`http:// *[!DNL server]*/ir/render/'`），但可能包含前置處理規則權杖。

在巢狀要求中指定下列命令時（在要求URL中或在`catalog::Modifier`或`catalog::PostModifier`中），會忽略這些命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

同樣被忽略的是套用至巢狀轉譯器要求的材質目錄的`attribute::MaxPix`和`attribute::DefaultPix`。

巢狀IR要求的影像結果可透過包含`cache=on`選擇性地進行快取。 依預設，會停用中繼資料的快取。 只有在合理時段內於不同請求中重複使用中間影像時，才應啟用快取。 標準伺服器端快取管理適用。 資料會以無損格式快取。
