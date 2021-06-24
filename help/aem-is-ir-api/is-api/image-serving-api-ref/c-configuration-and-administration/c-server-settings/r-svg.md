---
description: 只有在需要SVG呈現時，才需要考慮此區段中的設定。
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---

# SVG{#svg}

只有在需要SVG呈現時，才需要考慮此區段中的設定。

## SV::SvgHeapSize - SVG堆大小 {#section-59ab17681daa4be8b5d794713e1a504e}

SVG轉譯器的Java堆大小。 預設為「200m」(200 MB)。

## PS::svgProvider.rootPaths - SVG資料根資料夾 {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG源資料檔案的位置。 可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的一個或多個絕對檔案路徑或路徑，用分號分隔。 通常設為與`IS::RootPath`相同的值。

## PS::svgProvider.SVGFileSizeLimit — 最大SVG檔案大小 {#section-b9c81e3e104642ebbdd9f000843d3256}

最大SVG源檔案大小（以kBytes為單位）。 嘗試呈現大於此限制的SVG檔案時，伺服器返回錯誤。 預設為1024千位元組。

## IS::SvgMAxRenderRgnPixels - SVG輸出影像大小限制 {#section-5be1fd9639424d878a5ffd11736d3920}

限制SVGRender可生成的影像的大小。 大於0的整數值（以百萬像素為單位）。 如果呈現操作超過大小限制，則返回錯誤。 預設為 4。

## PS::svgProvider.port — 平台伺服器監聽埠 {#section-f7e42a96c2dd4523b46f0557c239e659}

用於SvgRender從平台伺服器獲取要嵌入到SVG呈現的影像的埠。

重要資訊要正確運行SVGRender元件，必須將此配置選項設定為與`TC::PsPort`相同的值。

## PS::svgProvider.fontRoot - SVG字型檔案資料夾 {#section-a8d45b0d68504945b8780f5eac351b0d}

指定SvgRender將在何處查找呈現SVG文本所需的字型檔案；通常在`IS::RootPaths`中指定的路徑之一。 預設為[!DNL *[!DNL install_folder]*/images]。

## SVG::SVGRender.port, IS::SVGTcpPort - SVG通信埠 {#section-608687123aa644b7b58fe42385d71b79}

配置映像伺服器和SVGRender元件通信的埠。

>[!NOTE]
>
>為了SVGRender元件的正確運行，必須為`SVG::SVGRender.port`和`IS::SVGTcpPort`指定相同的埠號。
