---
description: 支援四種類型的圖層。
seo-description: 支援四種類型的圖層。
seo-title: 圖層類型
solution: Experience Manager
title: 圖層類型
topic: Scene7 Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 圖層類型{#layer-types}

支援四種類型的圖層。

## 影像圖層 {#section-3e53df1437694272aca03f927fc0db07}

影像圖層必須 `src=` 有指定要用作圖層的影像的命令。 可以指定單獨的圖 `mask=` 像作為圖層遮色片，或者該影像已經具有Alpha色版。 影像圖層的大小一律是從影像中衍生而來，但是影像通常會使用指令縮放以符合 `size=` 大小。 剪輯路徑可以與一起應用 `clipPath=`。

## 文字圖層 {#section-dc2aec6416a340bcb20c1f884323c8d0}

必須有 `text=` 或命 `textPs=` 令，該命令以富文本格式(RTF)文本片段的形式提供文本內容。 文字圖層可依其內容自行調整大小，或可以指定明確的大小（例如，如果要將文字包住特定寬度，或文字必須限制在特定區域內）。 `textPs=` 支援將文字流入使用定義的任意形狀， `textFlowPath=` 並移入使用定義的任意路徑 `textPath=`。 `textPs=` 也支援將文字轉換為文字方塊或以任意角度( `textAngle=`)指定形狀。

## 純色圖層 {#section-56dfb672756643dda08dc93294809eb0}

範本中的圖層0通常使用純色圖層，因此複合影像的大小是固定的，且與任何影像內容無關。 實色圖層需要一 `color=` 個屬性，或 `size=` ，並支 `mask=`持大多數其它命令和屬性來修改外觀。 可使用任意形狀來指定純色圖層 `clipPath=`。

## 效果圖層 {#section-dd3b628bc6734077af4c0ddcebcee05f}

IS會使用特殊的子圖層來建置Photoshop樣式的圖層效果，例如陰影和發光效果，這些子圖層可附加至影像、文字和純色圖層。 這些效果圖層繼承父圖層遮色片和父圖層的位置，而且功能有限。
