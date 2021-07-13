---
description: 檢視影像轉換
solution: Experience Manager
title: 檢視影像轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 檢視影像轉換{#view-transform-for-images}

回應`req=img`要求而傳回給用戶端的影像，會考量下列值，從複合影像衍生而來：`wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix`和複合影像的大小。

如果指定了`wid=`和`hei=`，但未指定`scl=`，則會縮放複合影像，使其完全適合於`wid=`和`hei=`所定義的視圖直接內。 如果視圖直角的長寬比與複合影像的長寬比不同，則使用`align=`值（如果指定）在視圖直角內對齊縮放的複合影像，否則會將其置中。 影像資料未覆蓋的任何空間都會填入`bgc=`，若未指定，則會填入`attribute::BkgColor`。

如果指定`scl=`，則複合影像將按該縮放因子縮放。 如果也指定了`wid=`和/或`hei=`，則縮放影像隨後被裁切到`wid=`和/或`hei=`，或根據需要添加額外空間。 `align=` 指定影像被裁切或新增額外空間的位置，且任何額外空間都會填 `bgc=` 入或 `attribute::BkgColor`。

如果未指定`wid=`、`hei=`或`scl=`，並且如果複合影像的寬度或高度超過`attribute::DefaultPix`，則複合影像會縮放至不超過`attribute::DefaultPix`。 否則，將使用複合影像而不縮放。

要保證返回視圖影像而不進行任何進一步縮放，請指定`scl=1`。

如果指定`rgn=`，則回覆影像隨後相應地被裁切，以達到最終的回覆影像大小。 此大小會與`attribute::MaxPix`（如果已定義）比較，如果回覆影像在任一維度中較大，則會產生錯誤。

如果`fmt=`指定了不含Alpha的資料，則回復影像中的任何透明區域都將填充`bgc=`或`attribute::BkgColor`。
