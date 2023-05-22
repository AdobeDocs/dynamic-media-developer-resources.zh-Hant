---
description: 支援四種類型的層。
solution: Experience Manager
title: 層類型
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 層類型{#layer-types}

支援四種類型的層。

## 影像層 {#section-3e53df1437694272aca03f927fc0db07}

影像層必須具有 `src=` 命令，該命令指定要用作圖層的影像。 可以使用 `mask=` 將用作圖層蒙版或影像可能已具有α通道。 影像層的大小總是從影像中導出，但影像通常會使用 `size=` 的子菜單。 可應用剪輯路徑 `clipPath=`。

## 文本圖層 {#section-dc2aec6416a340bcb20c1f884323c8d0}

必須有 `text=` 或 `textPs=` 命令，該命令以富格文本格式(RTF)文本片段的形式提供文本內容。 文本圖層可以根據其內容進行自調整大小，也可以指定顯式大小（例如，如果文本要換行到特定寬度，或者文本必須限制在特定區域內）。 `textPs=` 支援將文本流入定義為任意形狀 `textFlowPath=` 和 `textPath=`。 `textPs=` 還支援以任意角度將文本渲染到文本框或指定形狀( `textAngle=`)。

## 實色層 {#section-56dfb672756643dda08dc93294809eb0}

實色層通常用於模板中的第0層，因此複合影像的大小是固定的並且與任何影像內容無關。 實色層要求 `color=` 屬性和 `size=` 或 `mask=`，並支援大多數其它命令和屬性來修改外觀。 可使用任意形狀指定實色層 `clipPath=`。

## 效果層 {#section-dd3b628bc6734077af4c0ddcebcee05f}

IS使用可附加到影像、文本和實色層的特殊子層來實現Photoshop式層效果，如投影和發光效果。 這些效果層繼承父層蒙版和父層的位置，並且功能有限。
