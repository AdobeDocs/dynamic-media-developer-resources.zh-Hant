---
description: 影像的檢視轉換
solution: Experience Manager
title: 影像的檢視轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 影像的檢視轉換{#view-transform-for-images}

回應`req=img`要求傳回給使用者端的影像是從複合影像衍生而來，考量了下列值： `wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix`以及複合影像的大小。

如果已指定`wid=`和`hei=`，但未指定`scl=`，則會縮放複合影像，使其完全符合`wid=`和`hei=`定義的檢視矩形。 如果檢視矩形的外觀比例與複合影像的外觀比例不同，則縮放後的複合影像會使用`align=`值在檢視矩形內對齊（若指定），否則會置中。 影像資料未涵蓋的任何空間會以`bgc=`填滿，如果未指定，則會以`attribute::BkgColor`填滿。

如果指定`scl=`，複合影像會以該縮放因子縮放。 如果同時指定`wid=`和/或`hei=`，則縮放的影像會視需要裁剪為`wid=`和/或`hei=`或增加額外的空間。 `align=`指定影像的裁切位置或新增額外空間，任何額外空間都會以`bgc=`或`attribute::BkgColor`填滿。

若未指定`wid=`、`hei=`或`scl=`，且複合影像的寬度或高度超過`attribute::DefaultPix`，則複合影像會縮放至不超過`attribute::DefaultPix`。 否則，不使用縮放即可使用複合影像。

若要確保檢視影像不會進一步縮放，請指定`scl=1`。

若指定`rgn=`，回覆影像會據此裁切，以得出最終的回覆影像大小。 將此大小與`attribute::MaxPix` （若已定義）進行比較，如果任一維度中的回覆影像較大，則會產生錯誤。

如果`fmt=`指定不含Alpha的資料，回覆影像中的任何透明區域都會以`bgc=`或`attribute::BkgColor`填滿。
